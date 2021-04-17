---
title: Mensaje de LB_ADDFILE (Winuser. h)
description: Agrega el nombre de archivo especificado a un cuadro de lista que contiene una lista de directorios.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492154"
---
# <a name="lb_addfile-message"></a>Mensaje de LB \_ ADDFILE

Agrega el nombre de archivo especificado a un cuadro de lista que contiene una lista de directorios.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero a un búfer que especifica el nombre del archivo que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero del archivo que se agregó, o LB \_ Err si se produce un error.

## <a name="remarks"></a>Observaciones

La función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) debe haber rellenado el cuadro de lista al que se agrega *lParam* .

El mensaje [**lb \_ INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes de la **lb \_** de la carga posterior tarden el menor tiempo posible. Puede usar estimaciones para los parámetros *wParam* e *lParam* . Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.

En el caso de una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP. Esto puede causar problemas. Por ejemplo, los caracteres romanos acentuados en un cuadro de lista no Unicode en las ventanas japonesas se desactivarán. Para solucionar este error, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> </dl>

 

 





