---
title: Método CreateEncryptor de IWMDRMLicense (Wmdrmsdk.h)
description: El método CreateEncryptor crea un objeto de cifrado con la configuración de la licencia actual.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- CreateEncryptor method windows Media Format
- Método CreateEncryptor windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interfaz windows Media Format , CreateEncryptor (método)
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481e33b6a3d4ffff3805ccc14f45b06a12ad2296fdaaedf13608f3a519c6ed10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433664"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>IWMDRMLicense::CreateEncryptor (método)

El **método CreateEncryptor** crea un objeto de cifrado con la configuración de la licencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEncryptor* \[ out\]
</dt> <dd>

Recibe un puntero a la [**interfaz IWMDRMEncrypt**](iwmdrmencrypt.md) del objeto recién creado.

</dd> </dl>

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
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





