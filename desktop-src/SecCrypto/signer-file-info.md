---
description: Especifica un archivo que se va a firmar.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Estructura de SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668480"
---
# <a name="signer_file_info-structure"></a>Estructura de \_ información del archivo del firmante \_

La estructura de **\_ \_ información del archivo del firmante** especifica el archivo que se va a firmar.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de la estructura, en bytes.

</dd> <dt>

**pwszFileName**
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre del archivo que se va a firmar.

</dd> <dt>

**hFile**
</dt> <dd>

Identificador abierto del archivo especificado por el miembro **pwszFileName** . Si este miembro contiene un identificador válido, este identificador se utiliza para obtener acceso al archivo. Este miembro se puede establecer en **null**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de \_ asunto del firmante \_**](signer-subject-info.md)
</dt> </dl>

 

 




