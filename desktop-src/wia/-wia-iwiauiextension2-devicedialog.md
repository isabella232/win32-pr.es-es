---
description: Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: IWiaUIExtension2::D método eviceDialog (Wiadevd. h)
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
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275455"
---
# <a name="iwiauiextension2devicedialog-method"></a>IWiaUIExtension2::D método eviceDialog

Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeviceDialogData* \[ de\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA2 \** _

Apunta a una estructura [_ *DEVICEDIALOGDATA2* *](-wia-devicedialogdata2.md) que contiene todos los datos necesarios para implementar el cuadro de diálogo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si el usuario cancela el cuadro de diálogo, el método devuelve S \_ false. Si se produce un error en el método, devuelve un código de error adecuado. En la tabla siguiente se muestran algunos de los códigos de estado devueltos posibles.



| Código de error    | Descripción                              |
|---------------|------------------------------------------|
| E \_ INVALIDARG | El parámetro pDeviceDialogData es **null**. |
| E \_ NOTIMPL    | El método no está implementado.           |



 

## <a name="remarks"></a>Observaciones

Si implementa la interfaz [**IWiaUIExtension2**](-wia-iwiauiextension2.md) y no desea reemplazar la interfaz de usuario del sistema, este método debe seguir implementado, pero no debe hacer nada más que devolver E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




