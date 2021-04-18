---
description: El registro es una base de datos jerárquica que contiene datos que son fundamentales para el funcionamiento de Windows y las aplicaciones y servicios que se ejecutan en Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Estructura del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b76b7f827ae3ea96d75d089c7d874c3d31d030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555390"
---
# <a name="structure-of-the-registry"></a>Estructura del registro

El registro es una base de datos jerárquica que contiene datos que son fundamentales para el funcionamiento de Windows y las aplicaciones y servicios que se ejecutan en Windows. Los datos se estructuran en un formato de árbol. Cada nodo del árbol se denomina *clave*. Cada clave puede contener *subclaves* y entradas de datos denominadas *valores*. A veces, la presencia de una clave son todos los datos que necesita una aplicación; otras veces, una aplicación abre una clave y utiliza los valores asociados a la clave. Una clave puede tener cualquier número de valores y los valores pueden estar en cualquier formato. Para obtener más información, vea [tipos de valor del registro](registry-value-types.md) y límites de tamaño de los [elementos del registro](registry-element-size-limits.md).

Cada clave tiene un nombre que se compone de uno o más caracteres imprimibles. Los nombres de clave no distinguen mayúsculas de minúsculas. Los nombres de clave no pueden incluir el carácter de barra diagonal inversa ( \) , pero se puede usar cualquier otro carácter imprimible. Los nombres de valor y los datos pueden incluir el carácter de barra diagonal inversa.

El nombre de cada subclave es único con respecto a la clave que está inmediatamente por encima en la jerarquía. Los nombres de clave no están localizados en otros lenguajes, aunque los valores pueden ser.

La siguiente ilustración es una estructura de clave del registro de ejemplo, tal como la muestra el editor del registro.

![ventana del editor del registro](images/regtree.png)

Cada uno de los árboles de **mi PC** es una clave. La clave del **\_ \_ equipo local HKEY** tiene las siguientes subclaves: **hardware**, **Sam**, **seguridad**, **software** y **sistema**. Cada una de estas claves a su vez tiene subclaves. Por ejemplo, la clave de **hardware** tiene las subclaves **Description**, **DEVICEMAP** y **RESOURCEMAP**; la clave **DEVICEMAP** tiene varias subclaves, incluido el **vídeo**.

Cada valor está formado por un nombre de valor y sus datos asociados, si los hay. **MaxObjectNumber** y **VgaCompatible** son valores que contienen datos en la subclave de **vídeo** .

Un árbol del registro puede tener un nivel de 512 niveles de profundidad. Puede crear hasta 32 niveles a la vez a través de una única llamada API del registro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el registro de Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
