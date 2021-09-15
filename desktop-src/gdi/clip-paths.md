---
description: Al igual que una región de recorte, una ruta de acceso de recorte es otro objeto gráfico que una aplicación puede seleccionar en un contexto de dispositivo.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Recortar rutas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359164"
---
# <a name="clip-paths"></a>Recortar rutas de acceso

Al igual que una región de recorte, una ruta de acceso de recorte es otro objeto gráfico que una aplicación puede seleccionar en un contexto de dispositivo. A diferencia de una región de recorte, una aplicación siempre crea un trazado de recorte y se usa para recortar una o varias formas irregulares. Por ejemplo, una aplicación puede usar las líneas y curvas que forman los contornos de los caracteres de una cadena de texto para definir una ruta de acceso de recorte.

Para crear una ruta de acceso de recorte, primero es necesario crear una ruta de acceso que describa la forma irregular necesaria. Las rutas de acceso se crean mediante una llamada a las funciones de dibujo de interfaz de dispositivo gráfico (GDI) adecuadas después de llamar a la función [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) y antes de llamar a [**la función EndPath.**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) Esta colección de funciones se denomina corchete de ruta de acceso. Para obtener más información sobre las rutas de acceso y los corchetes de acceso, vea [Rutas de acceso](paths.md).

Una vez creada la ruta de acceso, se puede convertir en una ruta de acceso de recorte llamando a la función [**SelectClipPath,**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) identificando un contexto de dispositivo y especificando un modo de uso. El modo de uso determina cómo combina el sistema la nueva ruta de acceso de recorte con la región de recorte original del contexto del dispositivo. En la tabla siguiente se describen los modos de uso.



| Mode      | Descripción                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| RGN \_ AND  | La ruta de acceso del clip incluye la intersección (áreas superpuestas) de la región de recorte del contexto del dispositivo y la ruta de acceso actual.    |
| COPIA DE RGN \_ | La ruta de acceso del clip es la ruta de acceso actual.                                                                                           |
| Diferencias de RGN \_ | La ruta de acceso del clip incluye la región de recorte del contexto del dispositivo con todas las partes de intersección de la ruta de acceso actual excluidas.        |
| RGN \_ O   | La ruta de acceso del clip incluye la unión (áreas combinadas) de la región de recorte del contexto del dispositivo y la ruta de acceso actual.              |
| RGN \_ XOR  | La ruta de acceso del clip incluye la unión de la región de recorte del contexto del dispositivo y la ruta de acceso actual, pero excluye la intersección. |



 

 

 



