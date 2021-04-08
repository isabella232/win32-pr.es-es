---
title: CLASS (instrucción)
description: Define la clase del cuadro de diálogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menús de instrucciones de clase y otros recursos
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995188"
---
# <a name="class-statement"></a>CLASS (instrucción)

Define la clase del cuadro de diálogo.

La instrucción de **clase** aparece en la sección opcional antes de la principal de una instrucción de [**cuadro de diálogo**](dialog-resource.md) . Si no se especifica ninguna clase, se utiliza la clase de cuadro de diálogo estándar.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*las*
</dt> <dd>

Entero de 16 bits sin signo o cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo. Si el procedimiento de ventana para la clase no procesa un mensaje que se le ha enviado, debe llamar a la función [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) para asegurarse de que todos los mensajes se controlan correctamente para el cuadro de diálogo. Una clase privada puede usar **DefDlgProc** como el procedimiento de ventana predeterminado. La clase se debe registrar con el miembro **cbWndExtra** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) establecida en **DLGWINDOWEXTRA**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La instrucción de **clase** solo se debe utilizar con casos especiales, ya que reemplaza el procesamiento normal de un cuadro de diálogo. La instrucción de **clase** convierte un cuadro de diálogo en una ventana de la clase especificada; dependiendo de la clase, esto podría dar resultados no deseados. No use los nombres de clase de control redefinidos con esta instrucción.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la instrucción de **clase** :

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
</dt> </dl>

 

 