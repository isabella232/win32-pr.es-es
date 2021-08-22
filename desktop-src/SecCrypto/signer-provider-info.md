---
description: Especifica el proveedor de servicios criptográficos (CSP) y la información de clave privada que se usa para crear una firma digital.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: SIGNER_PROVIDER_INFO estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 45ab23e4a568082de7e7fb4d23364ac6ba15c0f61378d54735cbc398e7e0e8ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898692"
---
# <a name="signer_provider_info-structure"></a>ESTRUCTURA DE INFORMACIÓN \_ DEL \_ PROVEEDOR DE FIRMANTE

La **estructura SIGNER \_ PROVIDER \_ INFO** especifica el proveedor [*de*](../secgloss/c-gly.md) servicios criptográficos (CSP) y la información de clave privada que se usa para crear una firma digital.

> [!Note]  
> Esta estructura no se define en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño, en bytes, de la estructura .

</dd> <dt>

**pwszProviderName**
</dt> <dd>

Nombre del CSP usado para crear la firma digital. Si el valor de este miembro es **NULL,** se usa el proveedor predeterminado.

</dd> <dt>

**dwProviderType**
</dt> <dd>

Tipo del CSP especificado por el **miembro pwszProviderName.**

</dd> <dt>

**dwKeySpec**
</dt> <dd>

Especificación de la clave. Si este miembro se establece en cero, se usa la especificación de clave en el **miembro pwszPvkFileName** o **pwszKeyContainer.** Si hay más de una especificación de clave en el **miembro pwszKeyContainer,** **se usa AT \_ SIGNATURE.** Si se produce un error, **se usa AT \_ KEYEXCHANGE.**

</dd> <dt>

**dwPvkChoice**
</dt> <dd>

Especifica el tipo de información de clave privada. Este miembro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                               | Significado                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**PVK \_ ESCRIBA \_ NOMBRE \_ DE ARCHIVO**</dt> <dt>1 (0x1)</dt> </dl>         | La información de clave privada es un nombre de archivo.<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**PVK \_ TYPE \_ KEYCONTAINER**</dt> <dt>2 (0x2)</dt> </dl> | La información de clave privada es un contenedor de claves.<br/> |



 

</dd> <dt>

**pwszPvkFileName**
</dt> <dd>

Nombre del archivo que contiene la información de clave privada.

</dd> <dt>

**pwszKeyContainer**
</dt> <dd>

Nombre del contenedor de claves que contiene la información de clave privada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
