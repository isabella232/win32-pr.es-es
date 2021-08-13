---
description: 'Método IWiaUIExtension2::D eviceDialog: proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.'
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: Método IWiaUIExtension2::D eviceDialog (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 582a2fe90e6a455b2c0d0119b749a9d86b912b58150d30f3804466ef5bea2a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439889"
---
# <a name="iwiauiextension2devicedialog-method"></a>IWiaUIExtension2::D eviceDialog (método)

Proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeviceDialogData* \[ En\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA2 \***

Apunta a una [**estructura DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) que contiene todos los datos necesarios para implementar el cuadro de diálogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si el método se realiza correctamente, devuelve S \_ OK. Si el usuario cancela el cuadro de diálogo, el método devuelve S \_ FALSE. Si se produce un error en el método, devuelve un código de error adecuado. En la tabla siguiente se muestran algunos de los códigos de estado de devolución posibles.



| Código de error    | Descripción                              |
|---------------|------------------------------------------|
| E \_ INVALIDARG | El parámetro pDeviceDialogData es **NULL.** |
| E \_ NOTIMPL    | El método no está implementado.           |



 

## <a name="remarks"></a>Observaciones

Si implementa la interfaz [**IWiaUIExtension2**](-wia-iwiauiextension2.md) y no desea reemplazar la interfaz de usuario del sistema, este método debe implementarse, pero no debe hacer nada más que devolver E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




