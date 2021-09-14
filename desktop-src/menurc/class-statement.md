---
title: Class (instrucción)
description: Define la clase del cuadro de diálogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menús de instrucción CLASS y otros recursos
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363518"
---
# <a name="class-statement"></a>Class (instrucción)

Define la clase del cuadro de diálogo.

La **instrucción CLASS** aparece en la sección opcional antes del main de una instrucción DIALOG. [](dialog-resource.md) Si no se proporciona ninguna clase, se usa la clase de diálogo estándar.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*Clase*
</dt> <dd>

Entero de 16 bits sin signo o una cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo. Si el procedimiento de ventana de la clase no procesa un mensaje enviado a ella, debe llamar a la función [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) para asegurarse de que todos los mensajes se administran correctamente para el cuadro de diálogo. Una clase privada puede usar **DefDlgProc como** procedimiento de ventana predeterminado. La clase debe registrarse con el **miembro cbWndExtra** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) establecida en **DLGWINDOWEXTRA**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **instrucción CLASS** solo debe usarse con casos especiales, ya que invalida el procesamiento normal de un cuadro de diálogo. La **instrucción CLASS** convierte un cuadro de diálogo en una ventana de la clase especificada; dependiendo de la clase , esto podría dar resultados no deseados. No use los nombres de clase de control redefinidos con esta instrucción.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción CLASS:**

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
</dt> </dl>

 

 