---
title: Método IWMDRMLicense GetNext (Wmdrmsdk.h)
description: El método GetNext carga la información sobre el siguiente elemento de la lista.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Formato multimedia de Windows del método GetNext
- Método GetNext windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interfaz windows Media Format , GetNext (método)
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc0905bc695d1317cc7e4a6a1933292ad68afa8f3e3aadb9572e7a7185f4089c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847142"
---
# <a name="iwmdrmlicensegetnext-method"></a>IWMDRMLicense::GetNext (Método)

El **método GetNext** carga la información sobre el siguiente elemento de la lista.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV DEMASIADO \_ \_ PEQUEÑO**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**ERROR \_ NO \_ MÁS \_ ELEMENTOS**</dt> </dl>      | En la lista no hay más elementos.<br/>          |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Comentarios

Los métodos de la [**interfaz IWMDRMLicense**](iwmdrmlicense.md) proporcionan datos sobre una licencia única a la vez. El objeto subyacente contiene una lista de una o varias licencias. Al llamar a este método, la interfaz mueve sus referencias internas a la siguiente licencia de la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





