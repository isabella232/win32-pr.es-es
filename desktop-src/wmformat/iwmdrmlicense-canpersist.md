---
title: Método IWMDRMLicense CanPersist (wmdrmsdk. h)
description: El método CanPersist consulta si la licencia puede conservarse en un almacén de licencias local.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Método CanPersist formato de Windows Media
- Método CanPersist formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método CanPersist
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708896"
---
# <a name="iwmdrmlicensecanpersist-method"></a>IWMDRMLicense:: CanPersist (método)

El método **CanPersist** consulta si la licencia puede conservarse en un almacén de licencias local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfCanPersist* \[ enuncia\]
</dt> <dd>

TRUE indica que la licencia puede conservarse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





