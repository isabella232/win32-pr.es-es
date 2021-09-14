---
title: ELEMENTO THEME
description: ELEMENTO THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Reproductor de Windows Media máscaras,elemento THEME
- skins,ELEMENTO THEME
- ELEMENTO THEME
- referencia de máscaras,elemento THEME
- elements,THEME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073194"
---
# <a name="theme-element"></a>ELEMENTO THEME

El **elemento THEME** es el elemento de nivel primario de una máscara y contiene uno o varios elementos **VIEW,** que a su vez contienen todos los demás elementos dentro de una máscara. Dentro del código de script, se tiene acceso al elemento **THEME** a través del atributo **global** de tema en lugar de a través de un nombre especificado por un atributo **id,** que no es compatible con el **elemento THEME.**

El **elemento THEME** admite los atributos siguientes.



| Atributo                                | Descripción                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Autor](theme-author.md)               | Especifica o recupera el nombre del autor de la máscara.                                                                      |
| [authorVersion](theme-authorversion.md) | Especifica o recupera el número de versión de la máscara según lo asignado por el autor.                                                |
| [Copyright](theme-copyright.md)         | Especifica o recupera la cadena de copyright de la máscara.                                                                       |
| [currentViewID](theme-currentviewid.md) | Especifica o recupera la vista mostrada **actualmente.**                                                                        |
| [title](theme-title.md)                 | Especifica o recupera el título de la máscara.                                                                                   |
| [version](theme-version.md)             | Especifica o recupera el número de Reproductor de Windows Media versión para el que se autorizó la máscara. Solo se puede establecer en tiempo de diseño. |



 

El **elemento THEME** admite los métodos siguientes.



| Método                                         | Descripción                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [closeView](theme-closeview.md)               | Cierra una vista **abierta.**                                                                                        |
| [loadPreference](theme-loadpreference.md)     | Carga una preferencia del Registro.                                                                           |
| [logString](theme-logstring.md)               | Registra una cadena definida por el usuario en el archivo de error, si el registro está habilitado.                                            |
| [openDialog](theme-opendialog.md)             | Abre un cuadro de diálogo de archivo.                                                                                        |
| [Openview](theme-openview.md)                 | Abre una **vista** en una nueva ventana.                                                                               |
| [openViewRelative](theme-openviewrelative.md) | Abre una **vista** en una nueva ventana en una posición inicial especificada con respecto a la esquina superior izquierda de la máscara. |
| [play Sound](theme-playsound.md)               | Reproduce el archivo de sonido especificado.                                                                                 |
| [savePreference](theme-savepreference.md)     | Guarda una preferencia en el Registro.                                                                             |
| [showErrorDialog](theme-showerrordialog.md)   | Muestra el cuadro de diálogo error estándar.                                                                         |



 

El **elemento THEME** no admite controladores de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




