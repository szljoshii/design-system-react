design-system-react
=====================

Future home of SLDS-React components

## Usage

```
npm install
npm start
open http://localhost:3000
```

## Tests

```
npm test
```

## Components

### Table of Contents
* [Buttons](#buttons)
* [Button Groups](#button-groups)
* [Lookups](#lookups)
* [Modals](#modals)
* [Picklists](#picklists)
* [Utility Icons](#utility-icons)


### [Buttons](https://www.lightningdesignsystem.com/components/buttons)

```jsx

import {SLDSButton} from 'design-system-react';

...

1. <SLDSButton label='Neutral' variant='neutral' onClick={this.handleNeutralClick} />
2. <SLDSButton label='Neutral Icon' variant='neutral' iconName='download' iconSize='small' iconPosition='right' onClick={this.handleNeutralClick} />
3. <SLDSButton label='Disabled' variant='neutral' disabled={true} onClick={this.handleDisabledClick} />
4. <SLDSButton label='Brand' variant='brand' onClick={this.handleBrandClick} />
5. <SLDSButton label='Settings' variant='icon' iconName='settings' iconSize='large' onClick={this.handleIconClick} />
6. <SLDSButton label='User' variant='icon' inverse={true} iconName='user' iconSize='large' onClick={this.handleIconClick} />
7. <SLDSButton label='Edit' variant='icon' hint={true} iconName='edit' iconSize='large' onClick={this.handleIconClick} />
8. <SLDSButton label='Follow' variant='neutral' stateful={true} notSelectedIcon='add' notSelectedLabel='Follow' selectedIcon='check' selectedLabel='Following' selectedFocusIcon='close' selectedFocusLabel='Unfollow' onClick={this.handleStatefulClick} />

Default Props             Prop Values
* label=undefined         * Required Prop
* variant='base'          ['base', 'neutral', 'brand', 'destructive', 'icon'] Use icon if you want an icon only button
* disabled=false
* tabindex=undefined
* inverse=false
* stateful=false
* responsive=false
* iconName=undefined      see https://www.lightningdesignsystem.com/resources/icons#utility for names
* className=undefined     custom classes on the button tag

** If iconName exists
  * iconVariant='bare'    ['bare', 'container', 'border', 'border-filled', 'small', 'more']
  * iconSize='medium'     ['x-small', 'medium', 'small', 'large']
  * iconPosition='left'   ['left', 'right', 'large'] If variant = icon, default icon position is centered.

** If stateful=true
  * notSelectedIcon=undefined
  * notSelectedLabel=undefined
  * selectedIcon=undefined
  * selectedLabel=undefined
  * selectedFocusIcon=undefined
  * selectedFocusLabel=undefined

```

[![browser support](/readme-assets/SLDSButtons.png)](/readme-assets/SLDSButtons.png)


### [Button Groups](https://www.lightningdesignsystem.com/components/button-groups)

```jsx

import {SLDSButtonGroup} from 'design-system-react';

...

<SLDSButtonGroup>
  <SLDSButton label='Refresh' variant='neutral' />
  <SLDSButton label='Edit' variant='neutral' />
  <SLDSButton label='Save' variant='neutral' />
  <SLDSButton label='More Options' variant='icon' iconName='down' iconVariant='border-filled' />
</SLDSButtonGroup>

<SLDSButtonGroup>
  <SLDSButton label='Chart' variant='icon' iconName='chart' iconVariant='border'/>
  <SLDSButton label='Filter' variant='icon' iconName='filter' iconVariant='border'/>
  <SLDSButton label='Sort' variant='icon' iconName='sort' iconVariant='more'/>
</SLDSButtonGroup>

```

[![browser support](/readme-assets/SLDSButtonGroups.png)](/readme-assets/SLDSButtonGroups.png)


### [Lookups](https://www.lightningdesignsystem.com/components/lookups)
#### *Base, single select only. Other variants coming soon.

```jsx

import {SLDSLookup} from 'design-system-react';

...

const items = [
  {label:'Paddy\'s Pub'},
  {label:'Tyrell Corp'},
  {label:'Paper St. Soap Company'},
  {label:'Nakatomi Investments'},
  {label:'Acme Landscaping'},
  {label:'Acme Construction'}
];

<SLDSLookup
  items={items}
  label="Account"
  type="account"
  headerRenderer={SLDSLookup.DefaultHeader}
  footerRenderer={SLDSLookup.DefaultFooter}
  onChange={this.onChange}
  onItemSelect={this.selectItem}
  />

```

[![browser support](/readme-assets/SLDSLookups.gif)](/readme-assets/SLDSLookups.gif)


### [Modals](https://www.lightningdesignsystem.com/components/modals)

```jsx

import {SLDSButton} from 'design-system-react';
import {SLDSModal} from 'design-system-react';

...

<SLDSButton label='Open Modal' variant='brand' onClick={this.openModal} />

<SLDSModal
  isOpen={this.state.modalIsOpen}
  title={<span>Lightning Design System: Style with Ease</span>}
  footer={[
    <SLDSButton key='cancelBtn' label='Cancel' variant='neutral' onClick={this.closeModal} />,
    <SLDSButton key='saveBtn' label='Save' variant='brand' onClick={this.handleSubmitModal} />
  ]}
  onRequestClose={this.closeModal}>
  {this.getModalContent()}
</SLDSModal>

```

[![browser support](/readme-assets/SLDSModals.gif)](/readme-assets/SLDSModals.gif)


### [PickLists](http://www.lightningdesignsystem.com/components/picklists#base&role=regular&status=all)
#### *Base only. Other variants coming soon.

```jsx

import {SLDSPicklistBase} from 'design-system-react';

...

const options = [
      {label:'A Option',value:'A0'},
      {label:'B Option',value:'B0'},
      {label:'C Option',value:'C0'},
      {label:'D Option',value:'D0'},
    ];

<SLDSPicklistBase options={options} label="Contacts" placeholder="Select a contact"/>

```

[![browser support](/readme-assets/SLDSPicklistBase.gif)](/readme-assets/SLDSPicklistBase.gif)


### [Utility Icons](https://www.lightningdesignsystem.com/resources/icons#utility)

```jsx

import {SLDSUtilityIcon} from 'design-system-react';

...

<SLDSUtilityIcon name='adduser' className='slds-input__icon slds-icon-text-default'/>

```

[![browser support](/readme-assets/SLDSUtilityIcons.png)](/readme-assets/SLDSUtilityIcons.png)


## Work in progress

### [DatePickers (base)](http://www.lightningdesignsystem.com/components/datepickers#base)

[![browser support](/readme-assets/SLDSDatePickerBase.gif)](/readme-assets/SLDSDatePickerBase.gif)



