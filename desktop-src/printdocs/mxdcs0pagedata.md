---
description: La \_ estructura MXDC S0PAGE \_ Data \_ T contiene una página de documento XPS que se pasará al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: MXDC_S0PAGE_DATA_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815347"
---
# <a name="mxdc_s0page_data_t-structure"></a>MXDC \_ S0PAGE \_ Data \_ T estructura

La estructura **MXDC \_ S0PAGE \_ Data \_ T** contiene una página de documento XPS que se pasará al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tamaño del búfer de salida, **bData**.

</dd> <dt>

**bData**
</dt> <dd>

Página del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se anexa a una estructura [**\_ t de \_ encabezado \_ de escape MXDC**](mxdcescapeheader.md) (que tiene el código de **operación** establecido en MXDCOP \_ set \_ S0PAGE) para crear una estructura [**MXDC \_ S0PAGE \_ PASSTHROUGH \_ escape \_ T**](mxdcs0pagepassthroughescape.md) . A continuación, esa estructura se pasa al parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con [**MXDC \_ escape**](mxdc-escape.md) como escape. El resultado es que el MXDC pasa la página a la salida sin procesarla.

La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

La aplicación que realiza la llamada es responsable de validar el XML de la página del documento XPS.

El consumo de streaming es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ set \_ S0PAGE \_ Resource** como **opCode** para cada recurso de la página antes de llamarlo con **MXDCOP \_ set \_ S0PAGE**.

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

 

