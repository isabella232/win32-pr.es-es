---
description: Recupera un valor que determina si la directiva de Device Guard confía en el código dinámico de .NET CRL en memoria o en disco especificado.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Función WldpQueryDynamicCodeTrust (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 00b26c8d237a8c6d725751be064c7b82fc7a600c452598a590a747ba10ae56d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075729"
---
# <a name="wldpquerydynamiccodetrust-function"></a>Función WldpQueryDynamicCodeTrust

Recupera un valor que determina si la directiva de Device Guard confía en el código dinámico de .NET CRL en memoria o en disco especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fileHandle* 
</dt> <dd>

Controle el archivo de código dinámico en disco que se comprobará. Si *fileHandle* no es **NULL,** *baseImage* debe ser **NULL.**

</dd> <dt>

*baseImage* 
</dt> <dd>

Puntero al archivo PE en memoria que se comprobará. Si *baseImage* no es **NULL,** *FileHandle* debe ser **NULL.**

</dd> <dt>

*ImageSize* 
</dt> <dd>

Cuando *baseImage* no es **NULL,** indica el tamaño de búfer al que *apunta baseImage.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ OK si se** realiza correctamente o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




