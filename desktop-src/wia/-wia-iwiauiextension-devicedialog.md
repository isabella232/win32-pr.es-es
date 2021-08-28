---
description: 'Método IWiaUIExtension::D eviceDialog: proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.'
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: IWiaUIExtension::D eviceDialog (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: a06ac5428743c31bae22c6d106ee927791739295754b15ac9764045c3aeeffab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813875"
---
# <a name="iwiauiextensiondevicedialog-method"></a>IWiaUIExtension::D eviceDialog (método)

Proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeviceDialogData* \[ En\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA \***

Apunta a una [**estructura DEVICEDIALOGDATA**](-wia-devicedialogdata.md) que contiene todos los datos necesarios para implementar el cuadro de diálogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si el método se realiza correctamente, devuelve S \_ OK. Si el usuario cancela el cuadro de diálogo, el método devuelve S \_ FALSE. Si el método no se implementa, devuelve E \_ NOTIMPL. Si se produce un error en el método, devuelve un código de error COM estándar.

## <a name="remarks"></a>Comentarios

Si implementa la interfaz [**IWiaUIExtension**](-wia-iwiauiextension.md) y no desea reemplazar la interfaz de usuario del sistema, este método todavía debe implementarse, pero no debe hacer nada más que devolver E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




