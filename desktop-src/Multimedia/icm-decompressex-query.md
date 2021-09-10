---
title: ICM_DECOMPRESSEX_QUERY mensaje (Vfw.h)
description: El ICM mensaje DECOMPRESSEX QUERY consulta un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede \_ descomprimir un formato de entrada específico a un formato de salida \_ específico.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- ICM_DECOMPRESSEX_QUERY mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370525"
---
# <a name="icm_decompressex_query-message"></a>\_ICM Mensaje DE DECOMPRESSEX \_ QUERY

El ICM mensaje **\_ DECOMPRESSEX \_ QUERY** consulta un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede descomprimir un formato de entrada específico a un formato de salida específico.


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Puntero a una [**estructura ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contiene el formato de entrada.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





