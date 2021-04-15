---
title: Estructura READERMODEINFO
description: Contiene la información necesaria para inicializar la función DoReaderMode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- READERMODEINFO estructura de Windows (controles)
- PREADERMODEINFO controles de Windows de puntero de estructura
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491746"
---
# <a name="readermodeinfo-structure"></a>Estructura READERMODEINFO

\[**READERMODEINFO** se admite a través de Windows XP con Service Pack 2 (SP2). Es posible que no se admita en versiones posteriores.\]

Contiene la información necesaria para inicializar la función [**DoReaderMode**](doreadermode.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obligatorio. Tamaño de la estructura, en bytes. Establezca este parámetro en **sizeof (READERMODE)** antes de llamar a [**DoReaderMode**](doreadermode.md).

</dd> <dt>

**identificador**
</dt> <dd>

Tipo: **[ **hWnd**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obligatorio. Identificador de la ventana que se va a usar para el modo de lectura.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Marcas que personalizan la funcionalidad de la ventana de modo de lector. Este parámetro puede ser 0; de lo contrario, uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                  | Significado                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <dt>**RMF \_ ZEROCURSOR**</dt> <dt>0x01</dt> </dl>             | Establece el cursor en el centro del área especificada en **PRC**. Si no se especifica esta marca, la posición del cursor permanece sin cambios.<br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <dt>**RMF \_ VERTICALONLY**</dt> <dt>0x02</dt> </dl>       | Solo permite el desplazamiento vertical.<br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <dt>**RMF \_ HORIZONTALONLY**</dt> <dt>0x04</dt> </dl> | Solo permite el desplazamiento horizontal.<br/>                                                                                                     |



 

</dd> <dt>

**PRC**
</dt> <dd>

Tipo: **LPRECT**

</dd> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica el área de desplazamiento en la ventana del modo lector. Si este miembro es **null**, se utiliza la ventana completa como área de desplazamiento.

</dd> <dt>

**pfnScroll**
</dt> <dd>

Tipo: **PFNREADERSCROLL**

</dd> <dd>

Un puntero a una función de devolución de llamada de [*ReaderScroll*](readerscroll.md) definida por la aplicación que se usa para notificar a la aplicación que la ventana debe desplazarse en una dirección determinada.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **PFNREADERTRANSLATEDISPATCH**

</dd> <dd>

Puntero a una función de devolución de llamada de [*TranslateDispatch*](translatedispatch.md) definida por la aplicación que se usa para obtener la primera notificación de los mensajes enviados a la ventana del modo de lectura.

</dd> <dt>

**lParam**
</dt> <dd>

Tipo: **[ **lParam**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Información adicional según sea necesario para la aplicación, leída por el autor de la llamada en la función de devolución de llamada [*ReaderScroll*](readerscroll.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no se declara en ningún encabezado público. Para usarlo, debe incluir la declaración mostrada anteriormente en su propio encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, \[ solo aplicaciones de escritorio de Windows Vista\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>          |



 

