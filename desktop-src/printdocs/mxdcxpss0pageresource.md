---
description: La \_ estructura de recursos T de MXDC XPS \_ S0PAGE \_ \_ contiene información sobre un recurso, como una imagen o fuente, que está asociada a una página de documento XPS y que se va a pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: MXDC_XPS_S0PAGE_RESOURCE_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910489"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>MXDC \_ XPS \_ S0PAGE \_ \_ estructura T

La estructura de **\_ \_ \_ recursos \_ T de MXDC XPS S0PAGE** contiene información sobre un recurso, como una imagen o fuente, que está asociada a una página de documento XPS y que se va a pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tamaño total de esta estructura y del recurso al que señala.

</dd> <dt>

**dwResourceType**
</dt> <dd>

Un valor de tipo [**\_ \_ \_ enumeración de página MXDC S0**](mxdcs0pageenums.md) que indica el tipo de recurso, como una imagen TIFF o una fuente TrueType.

</dd> <dt>

**szUri**
</dt> <dd>

URI del recurso. No puede tener más de 260 bytes.

</dd> <dt>

**dwDataSize**
</dt> <dd>

Tamaño del recurso en bytes.

</dd> <dt>

**bData**
</dt> <dd>

Los datos del recurso en una matriz de bytes con el tamaño 1 + el tamaño del recurso.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se anexa a una estructura [**\_ t de \_ encabezado \_ de escape MXDC**](mxdcescapeheader.md) (que tiene el **código de operación** establecido en **MXDCOP \_ set \_ S0PAGERESOURCE**) para crear una estructura de [**\_ \_ \_ escape \_ t de recurso MXDC S0PAGE**](mxdcs0pageresourceescape.md) . A continuación, se pasa la estructura de **\_ \_ \_ escape \_ T del recurso MXDC S0PAGE** resultante en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) a la que se llama con el escape de [**\_ escape MXDC**](mxdc-escape.md) . El efecto es enviar el recurso a MXDC para la conversión y escribir en el archivo de salida.

La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); sin embargo, puede haber más de una llamada de este tipo entre las llamadas a **StartPage** y **EndPage**.

El consumo de transmisión por secuencias es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el **código de operación** **MXDCOP \_ set \_ S0PAGE \_** para cada recurso de la página antes de llamar a **ExtEscape** con el **código de operación** MXDCOP **\_ set \_ S0PAGE** .

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

 

