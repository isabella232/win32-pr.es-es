---
description: 'Método IWiaUIExtension2::GetDeviceIcon: obtiene un icono de dispositivo personalizado.'
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: Método IWiaUIExtension2::GetDeviceIcon (Wiadevd.h)
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
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116623"
---
# <a name="iwiauiextension2getdeviceicon-method"></a>IWiaUIExtension2::GetDeviceIcon (método)

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

*bstrDeviceId* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador de dispositivo del dispositivo WIA para el que se va a obtener el icono.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Tipo: **HICON \***

Apunta a una ubicación de memoria que recibirá un identificador para el icono del dispositivo.

</dd> <dt>

*nSize* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Especifica el tamaño de icono deseado, en píxeles. Se supone que el icono es cuadrado y nSize especifica el ancho y el alto del icono solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error en el método, devuelve un código de error adecuado. En la tabla siguiente se muestran algunos de los códigos de estado de devolución posibles.



| Código de error    | Descripción                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | El parámetro bstrDeviceId o phIcon **es NULL** o bstrDeviceId no apunta a una cadena de identificador de dispositivo WIA válida |
| E \_ FAIL       | No hay ningún recurso de icono disponible.                                                                               |
| E \_ NOTIMPL    | No hay ningún icono del tamaño solicitado disponible.                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




