---
title: Método IWMDRMLicense ResetEnumeration (Wmdrmsdk.h)
description: El método ResetEnumeration restablece la lista de licencias a su estado original. La licencia activa se convierte en la primera licencia de la lista.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- ResetEnumeration method windows Media Format
- Método ResetEnumeration windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interfaz windows Media Format , ResetEnumeration (método)
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dda6de46a2ce96d1fec1abaaae56edcbc5b0d6a73e8ee13f038dba6b5577c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027693"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a>IWMDRMLicense::ResetEnumeration (método)

El **método ResetEnumeration** restablece la lista de licencias a su estado original. La licencia activa se convierte en la primera licencia de la lista.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV DEMASIADO \_ \_ PEQUEÑO**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





