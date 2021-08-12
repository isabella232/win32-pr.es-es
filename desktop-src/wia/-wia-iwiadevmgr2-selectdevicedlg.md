---
description: 'Método IWiaDevMgr2::SelectDeviceDlg: muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.'
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: Método IWiaDevMgr2::SelectDeviceDlg (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 344b13ec05e6f1d06011b3555e5b455202e5848b5000e799540d9f7c3160653b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441240"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>IWiaDevMgr2::SelectDeviceDlg (método)

Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
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

*pbstrDeviceID* \[ in, out\]
</dt> <dd>

Tipo: **BSTR \***

En la salida, recibe una cadena que contiene la cadena de identificador del dispositivo. En la entrada, pase la dirección de un puntero si esta información es necesaria o **NULL** si no es necesaria.

</dd> <dt>

*ppItemRoot* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero a la [**interfaz IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz del árbol jerárquico que representa el dispositivo WIA 2.0 seleccionado. Si no se encuentra ningún dispositivo, recibe **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                                  | Descripción                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | El dispositivo se seleccionó correctamente. <br/>                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | El usuario canceló el cuadro de diálogo. <br/>                                                              |
| <dl> <dt>**WIA \_ S NO HAY DISPOSITIVO \_ \_ \_ DISPONIBLE**</dt> </dl> | Ningún dispositivo de hardware WIA 2.0 coincide con las especificaciones indicadas en el *parámetro lDeviceType.* <br/> |



 

## <a name="remarks"></a>Observaciones

Este método crea y muestra el cuadro **de diálogo Seleccionar** dispositivo para que el usuario pueda seleccionar un dispositivo WIA 2.0 para la adquisición de imágenes. Si un dispositivo se selecciona correctamente, el método **IWiaDevMgr2::SelectDeviceDlg** crea un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para el dispositivo. Almacena un puntero a la **interfaz IWiaItem2** del elemento raíz en el parámetro *ppItemRoot*.

La aplicación puede restringir los dispositivos que se muestran al usuario a tipos concretos especificando los tipos de dispositivo mediante el *parámetro lDeviceType.* Si solo un dispositivo cumple la especificación, **IWiaDevMgr2::SelectDeviceDlg** no muestra el **cuadro de diálogo** Seleccionar dispositivo. En su lugar, crea el árbol [**IWiaItem2**](-wia-iwiaitem2.md) para el dispositivo y almacena un puntero a la **interfaz IWiaItem2** del elemento raíz en el *parámetro ppItemRoot*. Puede invalidar este comportamiento y forzar a **IWiaDevMgr2::SelectDeviceDlg** a mostrar el cuadro de diálogo especificando WIA SELECT DEVICE NODEFAULT como valor para el parámetro \_ \_ \_ *lFlags.* Si más de un dispositivo WIA 2.0 coincide con la  especificación, todos los dispositivos correspondientes se muestran en el cuadro de diálogo Seleccionar dispositivo para que el usuario pueda elegir uno.

Las aplicaciones deben llamar [al método IUnknown::Release en](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) los punteros de interfaz que reciben a través del parámetro *ppItemRoot.*

> [!Note]  
> Se recomienda que las aplicaciones hagan que la selección de dispositivos e imágenes esté disponible a través de un elemento de menú denominado **Desde escáner** en el **menú** Archivo.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
