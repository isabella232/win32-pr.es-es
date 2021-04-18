---
description: Especifica el proveedor de servicios criptográficos (CSP) y la información de clave privada utilizada para crear una firma digital.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Estructura de SIGNER_PROVIDER_INFO
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
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668197"
---
# <a name="signer_provider_info-structure"></a>Estructura de \_ información del proveedor de firmante \_

La estructura de **\_ \_ información del proveedor de firmante** especifica el proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) y la información de clave privada que se usa para crear una firma digital.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

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

Tamaño de la estructura, en bytes.

</dd> <dt>

**pwszProviderName**
</dt> <dd>

Nombre del CSP que se usa para crear la firma digital. Si el valor de este miembro es **null**, se utiliza el proveedor predeterminado.

</dd> <dt>

**dwProviderType**
</dt> <dd>

Tipo del CSP especificado por el miembro **pwszProviderName** .

</dd> <dt>

**dwKeySpec**
</dt> <dd>

Especificación de la clave. Si este miembro se establece en cero, se usa la especificación de clave en el miembro **pwszPvkFileName** o **pwszKeyContainer** . Si hay más de una especificación de clave en el miembro **pwszKeyContainer** , se usa **en la \_ firma** . Si se produce un error, se usa **en \_ KEYEXCHANGE** .

</dd> <dt>

**dwPvkChoice**
</dt> <dd>

Especifica el tipo de información de clave privada. Este miembro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                               | Significado                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**PVK \_ \_ \_ Nombre del archivo de tipo**</dt> <dt>1 (0x1)</dt> </dl>         | La información de clave privada es un nombre de archivo.<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**PVK \_ TIPO \_ keycontainer**</dt> <dt>2 (0X2)</dt> </dl> | La información de clave privada es un contenedor de claves.<br/> |



 

</dd> <dt>

**pwszPvkFileName**
</dt> <dd>

Nombre del archivo que contiene la información de la clave privada.

</dd> <dt>

**pwszKeyContainer**
</dt> <dd>

Nombre del contenedor de claves que contiene la información de la clave privada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
