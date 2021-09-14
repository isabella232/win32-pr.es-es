---
description: Control de Unicode en una IME-Aware aplicación
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Control de Unicode en una IME-Aware aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274607"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a>Control de Unicode en una IME-Aware aplicación

Hay dos problemas relacionados con IMM y su control de Unicode. El primer problema es que las versiones Unicode de las funciones de IMM recuperan el tamaño de un búfer en bytes en lugar de caracteres Unicode de 16 bits. El segundo problema es que IMM normalmente recupera caracteres Unicode (en lugar de caracteres DBCS) en los mensajes [**\_ WM CHAR**](../inputdev/wm-char.md) y WM [**\_ IME \_ CHAR.**](wm-ime-char.md)

Windows admite una interfaz Unicode para IMM, además de la interfaz ANSI que se admite originalmente.

Las aplicaciones deben usar [**RegisterClassW para**](/windows/win32/api/winuser/nf-winuser-registerclassa) hacer que los mensajes [**WM \_ CHAR**](../inputdev/wm-char.md) y [**WM \_ IME \_ CHAR**](wm-ime-char.md) recuperen caracteres Unicode en lugar de caracteres DBCS en el *parámetro wParam.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Administrador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 
