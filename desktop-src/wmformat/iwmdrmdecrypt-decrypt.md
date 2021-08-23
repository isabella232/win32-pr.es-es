---
title: Método IWMDRMDecrypt Decrypt (Wmdrmsdk.h)
description: El método Decrypt descifra un búfer de datos en su lugar.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Descifrar formato multimedia de windows del método
- Descifrar el método windows Media Format , IWMDRMDecrypt (interfaz)
- IWMDRMDecrypt interfaz windows Media Format , Decrypt (método)
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
ms.openlocfilehash: 7be82ec976da39103698b93a09b3d5235c8c8ee712783ca8284dc7b18c6a8a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027758"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>IWMDRMDecrypt::D ecrypt (método)

El **método Decrypt** descifra un búfer de datos en su lugar.

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

Datos que se descifrarán. Si el método se realiza correctamente, estos datos se descifran en la devolución.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

Tamaño de los datos en bytes.

</dd> <dt>

*pWMCryptoData* \[ En\]
</dt> <dd>

Puntero a una [**estructura WMDRMCryptoData**](wmdrmcryptodata.md) que contiene parámetros adicionales. Puede ser **NULL** si el contenido se ha cifrado con los parámetros predeterminados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMDecrypt (Interfaz)**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





