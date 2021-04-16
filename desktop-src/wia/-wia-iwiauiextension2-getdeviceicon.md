---
description: Obtiene un icono de dispositivo personalizado.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'IWiaUIExtension2:: GetDeviceIcon (método) (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541950"
---
# <a name="iwiauiextension2getdeviceicon-method"></a>IWiaUIExtension2:: GetDeviceIcon (método)

Obtiene un icono de dispositivo personalizado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDeviceId* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador del dispositivo WIA para el que se va a obtener el icono.

</dd> <dt>

*phIcon* \[ enuncia\]
</dt> <dd>

Tipo: **HICON \** _

Apunta a una ubicación de memoria que recibirá un identificador para el icono del dispositivo.

</dd> <dt>

_nSize * \[ en\]
</dt> <dd>

Tipo: **ULong**

Especifica el tamaño de icono deseado, en píxeles. Se supone que el icono es cuadrado y nSize especifica el ancho y el alto del icono solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error en el método, devuelve un código de error adecuado. En la tabla siguiente se muestran algunos de los códigos de estado devueltos posibles.



| Código de error    | Descripción                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | El parámetro bstrDeviceId o phIcon es **null**, o bstrDeviceId no apunta a una cadena de identificador de dispositivo WIA válida |
| E \_ FAIL       | No hay ningún recurso de icono disponible.                                                                               |
| E \_ NOTIMPL    | No hay disponible ningún icono del tamaño solicitado.                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




