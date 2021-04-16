---
description: Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'IWiaDevMgr2:: SelectDeviceDlgID (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705777"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>IWiaDevMgr2:: SelectDeviceDlgID (método)

Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Especifica la ventana primaria del cuadro de diálogo **seleccionar dispositivo** .

</dd> <dt>

*lDeviceType* \[ de\]
</dt> <dd>

Tipo: **Long**

Especifica el tipo de dispositivo WIA 2,0 que se va a usar. Vea [especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obtener una lista de valores posibles.

</dd> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Especifica el comportamiento del cuadro de diálogo. El valor puede ser uno de los siguientes.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Usa el comportamiento predeterminado.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ seleccionar \_ dispositivo \_ predeterminado**


</dt> <dd>

Mostrar el cuadro de diálogo aunque solo haya un dispositivo coincidente.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ out, retval\]
</dt> <dd>

Tipo: **BSTR \** _

Puntero a una cadena que recibe la cadena de identificador del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                                  | Descripción                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | El dispositivo se seleccionó correctamente. <br/>                                                          |
| <dl> <dt>**S \_ false**</dt> </dl>                      | El usuario canceló el cuadro de diálogo. <br/>                                                              |
| <dl> <dt>**WIA \_ S \_ no hay ningún \_ dispositivo \_ disponible**</dt> </dl> | Ningún dispositivo de hardware WIA 2,0 coincide con las especificaciones proporcionadas en el parámetro *lDeviceType* . <br/> |



 

## <a name="remarks"></a>Observaciones

Este método crea y muestra el cuadro de diálogo **seleccionar dispositivo** para que el usuario pueda seleccionar un dispositivo WIA 2,0 para la adquisición de imágenes. Si un dispositivo se selecciona correctamente, el método **IWiaDevMgr2:: SelectDeviceDlgID** pasa su cadena de identificador a la aplicación a través de su parámetro *pbstrDeviceID* .

La aplicación puede restringir los dispositivos que se muestran al usuario a determinados tipos especificando los tipos de dispositivo mediante el parámetro *lDeviceType* . Si solo un dispositivo cumple la especificación, **IWiaDevMgr2:: SelectDeviceDlgID** no muestra el cuadro de diálogo **seleccionar dispositivo** . En su lugar, pasa la cadena de identificador del dispositivo a la aplicación sin mostrar el cuadro de diálogo. Puede invalidar este comportamiento y forzar **IWiaDevMgr2:: SelectDeviceDlgID** para mostrar el cuadro de diálogo pasando WIA \_ SELECT \_ Device \_ nodefault como el valor del parámetro *lFlags* . Si más de un dispositivo WIA 2,0 coincide con la especificación, todos los dispositivos coincidentes se muestran en el cuadro de diálogo SelectDevice para que el usuario pueda elegir uno.

> [!Note]  
> Se recomienda que las aplicaciones hagan que la selección de dispositivos y imágenes esté disponible a través de un elemento de menú denominado **desde el escáner** en el menú **archivo** .

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




