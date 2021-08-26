---
title: Estructura LSKeyPack
description: Contiene información sobre un paquete de Servicios de Escritorio remoto de licencias específico.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Estructura LSKeyPack Servicios de Escritorio remoto
- Puntero de estructura LPLSKeyPack Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8b2c7c8b6c42464e273008f9de2730b41ea64981e44583eb48f4125da3ba9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989095"
---
# <a name="lskeypack-structure"></a>Estructura LSKeyPack

Contiene información sobre un paquete de Servicios de Escritorio remoto de licencias específico.

> [!Note]  
> Esta estructura no se define en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Versión del paquete de claves.

</dd> <dt>

**ucKeyPackType**
</dt> <dd>

Tipo de paquete de claves.

</dd> <dt>

**szCompanyName**
</dt> <dd>

Nombre de la empresa que emitió el paquete de claves.

</dd> <dt>

**szKeyPackId**
</dt> <dd>

Identificador del paquete de claves.

</dd> <dt>

**szProductName**
</dt> <dd>

Nombre del producto al que pertenece este paquete de claves.

</dd> <dt>

**szProductId**
</dt> <dd>

Identificador del producto al que pertenece este paquete de claves.

</dd> <dt>

**szProductDesc**
</dt> <dd>

Descripción del producto al que pertenece este paquete de claves.

</dd> <dt>

**wMajorVersion**
</dt> <dd>

Versión principal del producto al que pertenece este key pack.

</dd> <dt>

**wMinorVersion**
</dt> <dd>

Versión secundaria del producto al que pertenece este paquete de claves.

</dd> <dt>

**dwPlatformType**
</dt> <dd>

Tipo de plataforma.

</dd> <dt>

**ucLicenseType**
</dt> <dd>

Tipo de licencias en el paquete de claves.

</dd> <dt>

**dwLanguageId**
</dt> <dd>

Identificador de idioma.

</dd> <dt>

**ucChannelOfPurchase**
</dt> <dd>

Canal de compra.

</dd> <dt>

**szBeginSerialNumber**
</dt> <dd>

Número de serie de la primera licencia.

</dd> <dt>

**dwTotalLicenseInKeyPack**
</dt> <dd>

Número total de licencias del paquete de claves.

</dd> <dt>

**dwProductFlags**
</dt> <dd>

Banderas.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

Identificador del paquete de claves.

</dd> <dt>

**ucKeyPackStatus**
</dt> <dd>

Estado del paquete de claves.

</dd> <dt>

**dwActivateDate**
</dt> <dd>

Fecha de activación del paquete de claves.

</dd> <dt>

**dwExpirationDate**
</dt> <dd>

Fecha de expiración del paquete de claves.

</dd> <dt>

**dwNumberOfLicenses**
</dt> <dd>

Número de licencias.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

 





