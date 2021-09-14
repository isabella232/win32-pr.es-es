---
title: TB_ADDSTRING mensaje (Commctrl.h)
description: Agrega una nueva cadena al grupo de cadenas de la barra de herramientas.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166909"
---
# <a name="tb_addstring-message"></a>Mensaje \_ ADDSTRING de TB

Agrega una nueva cadena al grupo de cadenas de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Controle la instancia del módulo con un archivo ejecutable que contenga el recurso de cadena. Si *lParam en* su lugar apunta a una matriz de caracteres con una o varias cadenas, establezca este parámetro en **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de recurso para el recurso de cadena o puntero a una matriz TCHAR. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la primera cadena nueva si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Observaciones

Si *wParam* es **NULL,** *lParam* apunta a una matriz de caracteres con una o varias cadenas terminadas en NULL. La última cadena de la matriz debe terminar con dos caracteres NULL.

Si *wParam es* el HINSTANCE de la aplicación o de otro módulo que contiene un recurso de cadena, *lParam* es el identificador de recurso de la cadena. Cada elemento de la cadena debe comenzar con un carácter separador arbitrario y la cadena debe terminar con dos caracteres de este tipo. Por ejemplo, el texto de tres botones puede aparecer en la tabla de cadenas como "/New/Open/Save//". El mensaje devuelve el índice de "New" en el grupo de cadenas de la barra de herramientas y los demás elementos se encuentran en posiciones consecutivas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ ADDSTRINGW** (Unicode) y **TB \_ ADDSTRINGA** (ANSI)<br/>                 |



 

 





