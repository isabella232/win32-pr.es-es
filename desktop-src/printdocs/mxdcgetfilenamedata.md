---
description: La \_ estructura MXDC Get \_ filename \_ Data \_ T contiene la ruta de acceso completa y el nombre de archivo de un archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: MXDC_GET_FILENAME_DATA_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909581"
---
# <a name="mxdc_get_filename_data_t-structure"></a>MXDC \_ Get \_ filename \_ Data \_ T estructura

La estructura **MXDC \_ Get \_ filename \_ Data \_ T** contiene la ruta de acceso completa y el nombre de archivo de un archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbOutput**
</dt> <dd>

Tamaño del búfer de salida, **wszData**.

</dd> <dt>

**wszData**
</dt> <dd>

La ruta de acceso completa y el nombre de archivo del archivo de salida.

</dd> </dl>

## <a name="remarks"></a>Observaciones

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) devuelve esta estructura cuando se llama con el escape de [**\_ escape MXDC**](mxdc-escape.md) y la estructura [**MXDC de \_ \_ encabezado \_ de escape de**](mxdcescapeheader.md) que se pasa en el parámetro *lpszInData* tiene su código de **operación** establecido en **MXDCOP \_ Get \_ filename**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**\_escape MXDC**](mxdc-escape.md)
</dt> </dl>

 

