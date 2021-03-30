---
description: Recupera un valor que determina si la Directiva de Device Guard confía en el código dinámico de la CRL de .NET en memoria o en el disco.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Función WldpQueryDynamicCodeTrust (WLDP. h)
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
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538752"
---
# <a name="wldpquerydynamiccodetrust-function"></a>WldpQueryDynamicCodeTrust función)

Recupera un valor que determina si la Directiva de Device Guard confía en el código dinámico de la CRL de .NET en memoria o en el disco.

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

Identificador del archivo de código dinámico en disco que se va a comprobar. Si *FILEHANDLE* no es **null**, *baseImage* debe ser **null**.

</dd> <dt>

*baseImage* 
</dt> <dd>

Puntero al archivo PE en memoria que se va a comprobar. Si *baseImage* no es **null**, *FileHandle* debe ser **null**.

</dd> <dt>

*ImageSize* 
</dt> <dd>

Cuando *baseImage* no es **null**, indica el tamaño del búfer al que apunta *baseImage* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WLDP. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




