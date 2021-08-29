---
description: Control de Unicode en una IME-Aware aplicación
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Control de Unicode en una IME-Aware aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff5ea0953410a8f36098e5ac863c85e85fc7407163985995becd7c9e9233efa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829425"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a>Control de Unicode en una IME-Aware aplicación

Hay dos problemas relacionados con IMM y su control de Unicode. El primer problema es que las versiones Unicode de las funciones de IMM recuperan el tamaño de un búfer en bytes en lugar de caracteres Unicode de 16 bits. El segundo problema es que IMM normalmente recupera caracteres Unicode (en lugar de caracteres DBCS) en los mensajes [**\_ WM CHAR**](../inputdev/wm-char.md) y WM [**\_ IME \_ CHAR.**](wm-ime-char.md)

Windows admite una interfaz Unicode para IMM, además de la interfaz ANSI que se admite originalmente.

Las aplicaciones deben usar [**RegisterClassW para**](/windows/win32/api/winuser/nf-winuser-registerclassa) hacer que los mensajes [**WM \_ CHAR**](../inputdev/wm-char.md) y [**WM \_ IME \_ CHAR**](wm-ime-char.md) recuperen caracteres Unicode en lugar de caracteres DBCS en el *parámetro wParam.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Administrador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 
