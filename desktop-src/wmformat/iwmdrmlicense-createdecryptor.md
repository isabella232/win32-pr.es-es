---
title: Método CreateDecryptor de IWMDRMLicense (Wmdrmsdk.h)
description: El método CreateDecryptor crea un objeto decryptor con la configuración de la licencia actual.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- CreateDecryptor method windows Media Format
- Método CreateDecryptor windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interfaz windows Media Format , Método CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251457"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>IWMDRMLicense::CreateDecryptor (método)

El **método CreateDecryptor** crea un objeto decryptor con la configuración de la licencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDecryptor* \[ out\]
</dt> <dd>

Recibe un puntero a la [**interfaz IWMDRMDecrypt**](iwmdrmdecrypt.md) del objeto recién creado.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateEncryptor**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





