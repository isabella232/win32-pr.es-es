---
title: Método GetNext IWMDRMLicense (wmdrmsdk. h)
description: El método GetNext carga la información sobre el elemento siguiente de la lista.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Método GetNext formato de Windows Media
- Método GetNext formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetNext
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
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708648"
---
# <a name="iwmdrmlicensegetnext-method"></a>IWMDRMLicense:: GetNext (método)

El método **Getnext** carga la información sobre el elemento siguiente de la lista.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                | Descripción                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt> </dl> | Se necesita una lista de revocación de contenido actualizada.<br/> |
| <dl> <dt>**\_no hay \_ más \_ elementos de error**</dt> </dl>      | En la lista no hay más elementos.<br/>          |
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Los métodos de la interfaz [**IWMDRMLicense**](iwmdrmlicense.md) proporcionan datos sobre una sola licencia a la vez. El objeto subyacente contiene una lista de una o más licencias. Cuando se llama a este método, la interfaz mueve sus referencias internas a la siguiente licencia de la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





