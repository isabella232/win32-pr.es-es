---
description: Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: IWiaUIExtension::D método eviceDialog (Wiadevd. h)
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
ms.openlocfilehash: 7d42d0c7f8cca510a9c8f78de7bf589f8e1d2d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541955"
---
# <a name="iwiauiextensiondevicedialog-method"></a>IWiaUIExtension::D método eviceDialog

Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeviceDialogData* \[ de\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA \** _

Apunta a una estructura [_ *DEVICEDIALOGDATA* *](-wia-devicedialogdata.md) que contiene todos los datos necesarios para implementar el cuadro de diálogo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si el usuario cancela el cuadro de diálogo, el método devuelve S \_ false. Si no se implementa el método, devuelve E \_ NOTIMPL. Si se produce un error en el método, devuelve un código de error COM estándar.

## <a name="remarks"></a>Observaciones

Si implementa la interfaz [**IWiaUIExtension**](-wia-iwiauiextension.md) y no desea reemplazar la interfaz de usuario del sistema, este método debe seguir implementado, pero no debe hacer nada más que devolver E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




