---
title: Método Encrypt de IWMDRMEncrypt (wmdrmsdk. h)
description: El método Encrypt cifra un búfer de datos en contexto.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Método de cifrado de Windows Media Format
- Método Encrypt formato de Windows Media, interfaz IWMDRMEncrypt
- Interfaz IWMDRMEncrypt formato de Windows Media, método Encrypt
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718611"
---
# <a name="iwmdrmencryptencrypt-method"></a>IWMDRMEncrypt:: Encrypt (método)

El método **Encrypt** cifra un búfer de datos en contexto.

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

Datos que se van a cifrar. Si el método se ejecuta correctamente, los datos se cifran en la devolución.

</dd> <dt>

*cbData* \[ de\]
</dt> <dd>

Tamaño de los datos en bytes.

</dd> <dt>

*pWMCryptoData* \[ de\]
</dt> <dd>

Puntero a una estructura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contiene parámetros adicionales. Establezca en **null** para usar los valores de cifrado predeterminados.

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

[**Interfaz IWMDRMEncrypt**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





