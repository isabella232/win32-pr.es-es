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
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572169"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMEncrypt (interfaz)**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





