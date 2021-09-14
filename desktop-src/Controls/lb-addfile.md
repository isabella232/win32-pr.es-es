---
title: LB_ADDFILE mensaje (Winuser.h)
description: Agrega el nombre de archivo especificado a un cuadro de lista que contiene una lista de directorios.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061897"
---
# <a name="lb_addfile-message"></a>Mensaje \_ ADDFILE de LB

Agrega el nombre de archivo especificado a un cuadro de lista que contiene una lista de directorios.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que especifica el nombre del archivo que se agregará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero del archivo que se agregó o \_ LB ERR si se produce un error.

## <a name="remarks"></a>Observaciones

La función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) debe haber rellenado el cuadro de lista al que se agrega *lParam.*

El [**mensaje \_ LB INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes **\_ LB ADDFILE** subsiguientes tarden el menor tiempo posible. Puede usar estimaciones para los *parámetros wParam* *y lParam.* Si sobrestima, se asigna la memoria adicional; si se subvalora, se usa la asignación normal para los elementos que superan la cantidad solicitada.

Para una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP. Esto puede causar problemas. Por ejemplo, los caracteres latinos acentuados en un cuadro de lista no Unicode en japonés Windows aparecerán marcados. Para corregirlo, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> </dl>

 

 





