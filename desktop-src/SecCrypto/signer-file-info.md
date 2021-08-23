---
description: Especifica un archivo que se firmará.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: SIGNER_FILE_INFO estructura
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
ms.openlocfilehash: b0bb1bce810d87d70e05284e3d13942c5e2e49d07bd2d829c3839f793ae6a061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898831"
---
# <a name="signer_file_info-structure"></a>Estructura SIGNER \_ FILE \_ INFO

La **estructura SIGNER \_ FILE \_ INFO** especifica un archivo para firmar.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

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

Tamaño, en bytes, de la estructura .

</dd> <dt>

**pwszFileName**
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre del archivo que se firmará.

</dd> <dt>

**hFile**
</dt> <dd>

Identificador abierto para el archivo especificado por el **miembro pwszFileName.** Si este miembro contiene un identificador válido, este identificador se usa para tener acceso al archivo. Este miembro se puede establecer en **NULL.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DEL \_ FIRMANTE DEL \_ FIRMANTE**](signer-subject-info.md)
</dt> </dl>

 

 




