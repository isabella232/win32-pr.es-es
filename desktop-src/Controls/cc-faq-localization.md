---
title: Compatibilidad de localización con controles comunes
description: En este tema se describe la compatibilidad con idiomas nacionales integrados en los controles comunes.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994021"
---
# <a name="localization-support-for-common-controls"></a>Compatibilidad de localización con controles comunes

En este tema se describe la compatibilidad con idiomas nacionales integrados en los controles comunes. La compatibilidad integrada con el lenguaje nacional simplifica la implementación de aplicaciones localizadas.

Este tema contiene las siguientes secciones:

-   [Especificar un idioma para los controles comunes](#specifying-a-language-for-the-common-controls)
-   [Especificar un idioma para los controles de un cuadro de diálogo](#specifying-a-language-for-controls-in-a-dialog-box)
-   [Temas relacionados](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a>Especificar un idioma para los controles comunes

Si desea especificar un idioma para los controles comunes que son diferentes del idioma del sistema, llame a [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). El lenguaje especificado por esta función solo se aplica al proceso desde el que se llama a la función.

Para determinar el lenguaje que usan actualmente los controles comunes, llame a [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage). Devuelve el valor establecido por una llamada anterior a [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). El lenguaje devuelto es el que se especificó para el proceso del que se llama. Si no se ha llamado a **InitMUILanguage** o se llamó desde otro proceso, **GetMUILanguage** devolverá un valor predeterminado.

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a>Especificar un idioma para los controles de un cuadro de diálogo

A diferencia de los controles comunes, los controles predefinidos como botones o cuadros de edición no usan el idioma actual del sistema de forma predeterminada. El control de fuentes nativo es un control invisible que funciona en segundo plano para permitir que los controles predefinidos de un cuadro de diálogo muestren el idioma actual del sistema.

Para usar el control de fuente nativo, siga este procedimiento.

1.  Inicialice el control de fuentes nativo llamando a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). Establezca el miembro **dwICC** de la estructura [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) a la que apunta *lpInitCtrls* a la \_ clase NATIVEFNTCTL de ICC \_ .
2.  Agregue el control al script de recursos para el cuadro de diálogo. Establezca una o varias de las marcas de estilo siguientes para especificar los controles que se verán afectados. 

    | Marca              | Se aplica a                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | edición de NFS \_         | Controles de edición                                                                                                                                                                                                                                                    |
    | estática de NFS \_       | Controles estáticos                                                                                                                                                                                                                                                  |
    | \_LISTCOMBO NFS    | Controles List, ComboBox, List-View y ComboBoxEx                                                                                                                                                                                                               |
    | \_botón NFS       | Controles de botón                                                                                                                                                                                                                                                  |
    | \_todo NFS          | Todos los controles                                                                                                                                                                                                                                                     |
    | \_USEFONTASSOC NFS | Plataforma de Asia oriental. El control usa la característica de Asociación de fuentes en lugar de cambiar a la fuente nativa. Todas las demás plataformas lo omiten. Esto está en desuso para Windows Vista y no se admite en comctl V6. Esto existe en comctl V5 por motivos de herencia. |

    

     

En el ejemplo siguiente se muestra cómo agregar un control de fuente nativo a un script de recursos. Hace que los controles de edición, lista y cuadro combinado del cuadro de diálogo muestren texto con el idioma actual del sistema.


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles comunes](common-controls-intro.md)
</dt> </dl>

 

 




