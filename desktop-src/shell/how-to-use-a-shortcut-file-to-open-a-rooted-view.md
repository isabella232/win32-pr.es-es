---
description: Puede iniciar una vista con raíz de un punto de unión a través de un archivo de acceso directo a ese punto de unión.
title: Cómo abrir una vista raíz de un punto de unión a través de un archivo de acceso directo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581613"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a>Cómo abrir una vista raíz de un punto de unión a través de un archivo de acceso directo

Puede iniciar una vista con raíz de un punto de unión a través de un archivo [de acceso directo](./links.md) a ese punto de unión.

## <a name="instructions"></a>Instrucciones


Establezca la línea Destino del archivo de acceso directo en Explorer.exe con una marca /root. La forma exacta del comando depende de la ubicación del punto de unión:

-   Si el punto de unión es una subcarpeta del escritorio, use:

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   Si el punto de unión es una carpeta del sistema de archivos, use:

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   Si el punto de unión es una subcarpeta de una carpeta virtual del sistema, use:

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    Las carpetas virtuales del sistema que pueden contener puntos de unión tienen los siguientes identificadores de clase (CLID):

    

    | Carpeta del sistema     | Identificador de clase                       |
    |-------------------|----------------------------------------|
    | Mi PC       | {20D04FE0-3AEA-1069-A2D8-08002B30309D} |
    | Mis sitios de red | {208D2C60-3AEA-1069-A2D7-08002B30309D} |
    | Panel de control     | {21EC2020-3AEA-1069-A2DD-08002B30309D} |
    | Internet Explorer | {871C5380-42A0-1069-A2EA-08002B30309D} |

    

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar la ubicación de una extensión de espacio de nombres](nse-junction.md)
</dt> <dt>

[Cómo abrir una vista con raíz de un punto de unión a través del Registro](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
