---
title: Elemento THEME
description: Elemento THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Aspectos de Windows Media Player, elemento THEME
- máscaras, elemento de tema
- Elemento THEME
- referencia de las máscaras, elemento de tema
- elementos, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903282"
---
# <a name="theme-element"></a>Elemento THEME

El elemento de **tema** es el elemento de nivel primario de una máscara y contiene uno o varios elementos de **vista** que, a su vez, contienen todos los demás elementos de una máscara. En el código de script, se tiene acceso al elemento de **tema** mediante el atributo global de **tema** en lugar de un nombre especificado por un atributo de **identificador** , que no es compatible con el elemento de **tema** .

El elemento **Theme** admite los siguientes atributos.



| Atributo                                | Descripción                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [frente](theme-author.md)               | Especifica o recupera el nombre del autor de la máscara.                                                                      |
| [authorVersion](theme-authorversion.md) | Especifica o recupera el número de versión de la máscara tal como la asigna el autor.                                                |
| [sSoftware](theme-copyright.md)         | Especifica o recupera la cadena de copyright de la máscara.                                                                       |
| [currentViewID](theme-currentviewid.md) | Especifica o recupera la **vista** mostrada actualmente.                                                                        |
| [title](theme-title.md)                 | Especifica o recupera el título de la máscara.                                                                                   |
| [version](theme-version.md)             | Especifica o recupera el número de versión de Windows Media Player para el que se creó la máscara. Solo se puede establecer en tiempo de diseño. |



 

El elemento **Theme** admite los métodos siguientes.



| Método                                         | Descripción                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [closeView](theme-closeview.md)               | Cierra una **vista** abierta.                                                                                        |
| [loadPreference](theme-loadpreference.md)     | Carga una preferencia del registro.                                                                           |
| [logString](theme-logstring.md)               | Registra una cadena definida por el usuario en el archivo de error si está habilitado el registro.                                            |
| [openDialog](theme-opendialog.md)             | Abre un cuadro de diálogo de archivo.                                                                                        |
| [AbrirVista](theme-openview.md)                 | Abre una **vista** en una nueva ventana.                                                                               |
| [openViewRelative](theme-openviewrelative.md) | Abre una **vista** en una nueva ventana en la posición inicial especificada relativa a la esquina superior izquierda de la máscara. |
| [Reproducción](theme-playsound.md)               | Reproduce el archivo de sonido especificado.                                                                                 |
| [savePreference](theme-savepreference.md)     | Guarda una preferencia en el registro.                                                                             |
| [showErrorDialog](theme-showerrordialog.md)   | Muestra el cuadro de diálogo de error estándar.                                                                         |



 

El elemento **Theme** no admite controladores de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




