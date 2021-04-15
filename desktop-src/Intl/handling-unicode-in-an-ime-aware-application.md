---
description: Control de Unicode en una aplicación IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Control de Unicode en una aplicación IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688712"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a>Control de Unicode en una aplicación IME-Aware

Dos problemas están relacionados con el IMM y su control de Unicode. El primer problema es que las versiones Unicode de las funciones de IMM recuperan el tamaño de un búfer en bytes en lugar de caracteres Unicode de 16 bits. El segundo problema es que el IMM normalmente recupera caracteres Unicode (en lugar de caracteres DBCS) en los mensajes [**WM \_ Char**](../inputdev/wm-char.md) y [**WM \_ IME \_ Char**](wm-ime-char.md) .

Windows admite una interfaz Unicode para el IMM, además de la interfaz ANSI admitida originalmente.

Las aplicaciones deben usar [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) para que los mensajes de char de [**WM \_ Char**](../inputdev/wm-char.md) y [**WM \_ IME \_**](wm-ime-char.md) recuperen caracteres Unicode en lugar de caracteres DBCS en el parámetro *wParam* .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el administrador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 
