---
title: Mensaje de TB_ADDSTRING (commctrl. h)
description: Agrega una nueva cadena al grupo de cadenas de la barra de herramientas.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658407"
---
# <a name="tb_addstring-message"></a>Message TB de \_ ADDSTRING

Agrega una nueva cadena al grupo de cadenas de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la instancia de módulo con un archivo ejecutable que contiene el recurso de cadena. Si *lParam* en su lugar apunta a una matriz de caracteres con una o más cadenas, establezca este parámetro en **null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de recurso para el recurso de cadena o un puntero a una matriz TCHAR. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la primera cadena nueva si se realiza correctamente, o-1 en caso contrario.

## <a name="remarks"></a>Observaciones

Si *wParam* es **null**, *lParam* apunta a una matriz de caracteres con una o más cadenas terminadas en NULL. La última cadena de la matriz debe terminar con dos caracteres null.

Si *wParam* es el hInstance de la aplicación o de otro módulo que contiene un recurso de cadena, *lParam* es el identificador de recursos de la cadena. Cada elemento de la cadena debe comenzar por un carácter separador arbitrario y la cadena debe terminar con dos caracteres tales. Por ejemplo, el texto de tres botones podría aparecer en la tabla de cadenas como "/New/Open/Save//". El mensaje devuelve el índice de "New" en el grupo de cadenas de la barra de herramientas y los demás elementos están en posiciones consecutivas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ ADDSTRINGW** (Unicode) y **TB \_ ADDSTRINGA** (ANSI)<br/>                 |



 

 





