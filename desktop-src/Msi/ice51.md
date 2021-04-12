---
description: ICE51 comprueba que se ha proporcionado un título para los archivos de recursos de fuentes.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278159"
---
# <a name="ice51"></a>ICE51

ICE51 comprueba que se ha proporcionado un título para los archivos de recursos de fuentes.

Debe proporcionar un título para un recurso de fuente que no tenga un nombre incrustado. Solo los archivos de recursos de fuente. TTC,. ttf y. OTF no requieren un título, ya que estos archivos contienen un nombre incrustado. No proporcione un título para un recurso de fuente que contenga un nombre incrustado, ya que el sistema registra la fuente dos veces.

**[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** ICE51 no comprueba los archivos de recursos de fuente. OTF.

## <a name="result"></a>Resultado

ICE51 publica un error si hay archivos de recursos de fuentes. TTC,. ttf y. OTF con títulos. ICE51 publica una advertencia si hay otros archivos de recursos de fuente sin un título.

## <a name="example"></a>Ejemplo

ICE51 notificaría la siguiente advertencia para el ejemplo que se muestra.

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

ICE51 notificaría el siguiente mensaje de error para el ejemplo que se muestra.

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | FileName  |
|-------|-----------|
| Font1 | font1. ttf |
| Font2 | font2. fon |



 

[Tabla de fuentes](font-table.md)



| Archivo\_ | FontTitle          |
|--------|--------------------|
| Font1  | Una fuente realmente atractiva |
| Font2  |                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



