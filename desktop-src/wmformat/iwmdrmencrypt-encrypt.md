---
title: Método IWMDRMEncrypt Encrypt (Wmdrmsdk.h)
description: El método Encrypt cifra un búfer de datos en su lugar.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Cifrado del método windows Media Format
- Método encrypt windows Media Format , IWMDRMEncrypt (interfaz)
- IWMDRMEncrypt interface windows Media Format , Encrypt method
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb49b2857c23bb11b5e4d091dece820bb833b2b4e77224558f2d7972885445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027749"
---
# <a name="iwmdrmencryptencrypt-method"></a>IWMDRMEncrypt::Encrypt (Método)

El **método Encrypt** cifra un búfer de datos en su lugar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbData* \[ in, out\]
</dt> <dd>

Datos que se cifran. Si el método se realiza correctamente, los datos se cifran en la devolución.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

Tamaño de los datos en bytes.

</dd> <dt>

*pWMCryptoData* \[ En\]
</dt> <dd>

Puntero a una [**estructura WMDRMCryptoData**](wmdrmcryptodata.md) que contiene parámetros adicionales. Establezca en **NULL** para usar los valores de cifrado predeterminados.

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

[**IWMDRMEncrypt (interfaz)**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





