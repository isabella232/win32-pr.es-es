---
description: 'Método IWiaDevMgr2::SelectDeviceDlgID: muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.'
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: Método IWiaDevMgr2::SelectDeviceDlgID (Wia.h)
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
ms.openlocfilehash: a4279bef86d761ed0eb7d90ad3b8dee46e0f17f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106823"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>Método IWiaDevMgr2::SelectDeviceDlgID

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

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

Especifica la ventana primaria del cuadro **de diálogo Seleccionar** dispositivo.

</dd> <dt>

*lDeviceType* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica qué tipo de dispositivo WIA 2.0 se va a usar. Consulte [Especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obtener una lista de valores posibles.

</dd> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica el comportamiento del cuadro de diálogo. El valor puede ser uno de los siguientes.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Usa el comportamiento predeterminado.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**


</dt> <dd>

Muestra el cuadro de diálogo aunque solo haya un dispositivo correspondiente.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ out, retval\]
</dt> <dd>

Tipo: **BSTR \***

Puntero a una cadena que recibe la cadena de identificador del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                                  | Descripción                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | El dispositivo se seleccionó correctamente. <br/>                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | El usuario canceló el cuadro de diálogo. <br/>                                                              |
| <dl> <dt>**WIA \_ S NO HAY DISPOSITIVO \_ \_ \_ DISPONIBLE**</dt> </dl> | Ningún dispositivo de hardware WIA 2.0 coincide con las especificaciones indicadas en *el parámetro lDeviceType.* <br/> |



 

## <a name="remarks"></a>Comentarios

Este método crea y muestra el cuadro **de** diálogo Seleccionar dispositivo para que el usuario pueda seleccionar un dispositivo WIA 2.0 para la adquisición de imágenes. Si un dispositivo se selecciona correctamente, el método **IWiaDevMgr2::SelectDeviceDlgID** pasa su cadena de identificador a la aplicación a través de su *parámetro pbstrDeviceID.*

La aplicación puede restringir los dispositivos que se muestran al usuario a tipos concretos especificando los tipos de dispositivo mediante el *parámetro lDeviceType.* Si solo un dispositivo cumple la especificación, **IWiaDevMgr2::SelectDeviceDlgID** no muestra el **cuadro de diálogo** Seleccionar dispositivo. En su lugar, pasa la cadena de identificador del dispositivo a la aplicación sin mostrar el cuadro de diálogo. Puede invalidar este comportamiento y forzar que **IWiaDevMgr2::SelectDeviceDlgID** muestre el cuadro de diálogo pasando WIA SELECT DEVICE NODEFAULT como valor para el parámetro \_ \_ \_ *lFlags.* Si más de un dispositivo WIA 2.0 coincide con la especificación, todos los dispositivos correspondientes se muestran en el cuadro de diálogo Seleccionardispositivo para que el usuario pueda elegir uno.

> [!Note]  
> Se recomienda que las aplicaciones hagan que la selección de dispositivos e imágenes esté disponible a través de un elemento de menú denominado **Desde escáner** en **el menú** Archivo.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




