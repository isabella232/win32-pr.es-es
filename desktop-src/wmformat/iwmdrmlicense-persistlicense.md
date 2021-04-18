---
title: Método IWMDRMLicense PersistLicense (wmdrmsdk. h)
description: El método PersistLicense guarda la licencia actual del almacén temporal en el almacén de licencias local permanente.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Método PersistLicense formato de Windows Media
- Método PersistLicense formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método PersistLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708820"
---
# <a name="iwmdrmlicensepersistlicense-method"></a>IWMDRMLicense::P método ersistLicense

El método **PersistLicense** guarda la licencia actual del almacén temporal en el almacén de licencias local permanente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Si la licencia actual no está en el almacén temporal, se producirá un error en este método.

Puede llamar a [**CanPersist**](iwmdrmlicense-canpersist.md) para consultar si se permite que se conserve la licencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





