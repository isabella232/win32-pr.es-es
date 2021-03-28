---
description: Al igual que una región de recorte, una ruta de acceso de clip es otro objeto de gráficos que una aplicación puede seleccionar en un contexto de dispositivo.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Trazados de clip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985046"
---
# <a name="clip-paths"></a>Trazados de clip

Al igual que una región de recorte, una ruta de acceso de clip es otro objeto de gráficos que una aplicación puede seleccionar en un contexto de dispositivo. A diferencia de una región de recorte, una ruta de acceso de clip siempre la crea una aplicación y se usa para recortar a una o varias formas irregulares. Por ejemplo, una aplicación puede utilizar las líneas y curvas que forman los contornos de los caracteres de una cadena de texto para definir una ruta de acceso de recorte.

Para crear una ruta de acceso de clip, primero es necesario crear una ruta de acceso que describa la forma irregular necesaria. Las rutas de acceso se crean mediante una llamada a las funciones de dibujo de la interfaz de dispositivo gráfico (GDI) adecuadas después de llamar a la función [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) y antes de llamar a la función [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Esta colección de funciones se denomina corchete de ruta de acceso. Para obtener más información sobre las rutas de acceso y los corchetes de ruta, vea [rutas](paths.md).

Una vez creada la ruta de acceso, se puede convertir en una ruta de acceso de clip llamando a la función [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , identificando un contexto de dispositivo y especificando un modo de uso. El modo de uso determina la forma en que el sistema combina la nueva ruta de acceso del clip con la región de recorte original del contexto del dispositivo. En la tabla siguiente se describen los modos de uso.



| Mode      | Descripción                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| RGN \_ y  | La ruta de acceso del clip incluye la intersección (áreas superpuestas) de la región de recorte del contexto del dispositivo y la ruta de acceso actual.    |
| copia de RGN \_ | La ruta de acceso del clip es la ruta de acceso actual.                                                                                           |
| RGN ( \_ diferencia) | La ruta de acceso del clip incluye la región de recorte del contexto del dispositivo con las partes que interseccionan de la ruta de acceso actual excluida.        |
| RGN \_ o   | La ruta de acceso del clip incluye la Unión (áreas combinadas) de la región de recorte del contexto del dispositivo y la ruta de acceso actual.              |
| RGN \_ XOR  | La ruta de acceso del clip incluye la Unión de la región de recorte del contexto del dispositivo y la ruta de acceso actual, pero excluye la intersección. |



 

 

 



