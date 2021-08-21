---
description: La función DeleteExtractedFiles elimina los archivos extraídos por la función Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: Función DeleteExtractedFiles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 500de4df41c82f1956f50abcc25dc84f11484b693dc8d1a5f8bc53ab556ade0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162096"
---
# <a name="deleteextractedfiles-function"></a>Función DeleteExtractedFiles

\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.\]

La **función DeleteExtractedFiles** elimina los archivos extraídos por la [**función Extract.**](extract.md)

## <a name="syntax"></a>Sintaxis


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ps* 
</dt> <dd>

Puntero a una [**estructura SESSION**](session.md) que contiene información sobre la sesión actual.

Esta función libera la memoria en el miembro **pFileList** de esta estructura y establece **pFileList** en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Extracto**](extract.md)
</dt> <dt>

[**Sesión**](session.md)
</dt> </dl>

 

 
