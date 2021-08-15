---
description: El método GetPropById del objeto Item usa el identificador de una propiedad de elemento para devolver su valor.
ms.assetid: 00f7a91c-fd55-4016-a932-f710045a14b8
title: Método Item.GetPropById
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 5c8d5f68114f74505fce11ca8872370a802e31400159146d7030ec34339c7d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208379"
---
# <a name="itemgetpropbyid-method"></a>Método Item.GetPropById

El **método GetPropById** del [**objeto Item**](-wia-item.md) usa el identificador de una propiedad de elemento para devolver su valor.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Item.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id.* \[ en\]
</dt> <dd>

Tipo: **[WiaItemPropertyId](-wia-wiaitempropertyid.md)**

Especifica el identificador de la propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **VARIANT**

Este método devuelve el valor de la propiedad especificada por *id.*.

## <a name="remarks"></a>Comentarios

Use este método para buscar el valor de una propiedad de elemento a partir de su identificador. Para obtener una lista de los IDs de propiedad, vea [Definiciones de constantes de propiedad de WIA.](-wia-wia-property-constant-definitions.md) Para obtener información sobre las propias propiedades, vea [WiA Property Constants](-wia-wia-property-constants.md).

Para las aplicaciones Visual Basic Microsoft, agregue una referencia a "biblioteca de tipos Windows image acquisition 1.01". Las siguientes constantes definidas en ese archivo solo son válidas para los elementos raíz (elementos de dispositivo):

``` syntax
const FirmwareVersion = 1026
const ConnectStatus = 1027
const DeviceTime = 1028
const PicturesTaken = 2050
const PicturesRemaining = 2051
const ExposureMode = 2052
const ExposureCompensation = 2053
const ExposureTime = 2054
const FNumber = 2055
const FlashMode = 2056
const FocusMode = 2057
const FocusManualDist = 2058
const ZoomPosition = 2059
const PanPosition = 2060
const TiltPostion = 2061
const TimerMode = 2062
const TimerValue = 2063
const PowerMode = 2064
const BatteryStatus = 2065
const Dimension = 2070
const HorizontalBedSize = 3074
const VerticalBedSize = 3075
const HorizontalSheetFeedSize = 3076
const VerticalSheetFeedSize = 3077
const SheetFeederRegistration = 3078
const HorizontalBedRegistration = 3079
const VerticalBedRegistraion = 3080
const PlatenColor = 3081
const PadColor = 3082
const FilterSelect = 3083
const DitherSelect = 3084
const DitherPatternData = 3085
const DocumentHandlingCapabilities = 3086
const DocumentHandlingStatus = 3087
const DocumentHandlingSelect = 3088
const DocumentHandlingCapacity = 3089
const HorizontalOpticalResolution = 3090
const VerticalOpticalResolution = 3091
const EndorserCharacters = 3092
const EndorserString = 3093
const ScanAheadPages = 3094
const MaxScanTime = 3095
const Pages = 3096
const PageSize = 3097
const PageWidth = 3098
const PageHeight = 3099
const Preview = 3100
const TransparencyAdapter = 3101
const TransparecnyAdapterSelect = 3102
```

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso del **método GetPropById** para recuperar un valor de propiedad.


```JScript
<SCRIPT LANGUAGE="VBScript">
const DeviceType = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    objRootItem=objDeviceInfo.Create()
    objSelectedItems=objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItem
    PropValue = objItem.GetPropById(DeviceType)
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




