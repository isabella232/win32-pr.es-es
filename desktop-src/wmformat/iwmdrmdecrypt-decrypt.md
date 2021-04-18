---
title: Método de descifrado IWMDRMDecrypt (wmdrmsdk. h)
description: El método de descifrado descifra un búfer de datos en contexto.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Método de descifrado formato de Windows Media
- Método de descifrado formato de Windows Media, interfaz IWMDRMDecrypt
- Interfaz IWMDRMDecrypt formato de Windows Media, descifrar método
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718612"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>IWMDRMDecrypt::D método ECRYPT

El método de **descifrado** descifra un búfer de datos en contexto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbData* \[ in, out\]
</dt> <dd>

Datos que se van a descifrar. Si el método se ejecuta correctamente, estos datos se descifran en la devolución.

</dd> <dt>

*cbData* \[ de\]
</dt> <dd>

Tamaño de los datos en bytes.

</dd> <dt>

*pWMCryptoData* \[ de\]
</dt> <dd>

Puntero a una estructura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contiene parámetros adicionales. Puede ser **null** si el contenido se cifró con los parámetros predeterminados.

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

[**Interfaz IWMDRMDecrypt**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





