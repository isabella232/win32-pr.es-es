---
title: Mensaje de ICM_DECOMPRESSEX_QUERY (VFW. h)
description: El mensaje de consulta de DECOMPRESSEX ICM consulta \_ \_ un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede descomprimir un formato de entrada específico en un formato de salida específico.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- Mensaje de ICM_DECOMPRESSEX_QUERY de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905492"
---
# <a name="icm_decompressex_query-message"></a>Mensaje de consulta de \_ DECOMPRESSEX ICM \_

El mensaje de **\_ \_ consulta de DECOMPRESSEX ICM** consulta un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede descomprimir un formato de entrada específico en un formato de salida específico.


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Puntero a una estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contiene el formato de entrada.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
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
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





