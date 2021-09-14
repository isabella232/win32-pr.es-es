---
description: ICE07 valida que el paquete de instalación especifica que las fuentes se instalen en FontsFolder. Si se instala una fuente en una carpeta que no sea FontsFolder, el instalador crea un acceso directo en lugar de instalar realmente la fuente.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074674"
---
# <a name="ice07"></a>ICE07

ICE07 valida que el paquete de instalación especifica que las fuentes se instalen en FontsFolder. Si se instala una fuente en una carpeta que no sea FontsFolder, el instalador crea un acceso directo en lugar de instalar realmente la fuente.

La acción personalizada ICE07 hace lo siguiente para cada fuente de la [tabla Font](font-table.md).

1.  Busca el archivo de fuente al que pertenece cada título de fuente mediante la [tabla Font](font-table.md).
2.  Consulta la columna Component \_ de la tabla [File](file-table.md) para el componente que controla cada archivo.
3.  Consulta la columna Directory de la tabla Component para \_ obtener una clave en la tabla Directory. [](component-table.md)
4.  Resuelve la tabla [Directory para](directory-table.md) determinar el nombre de la carpeta en la que el instalador va a instalar el archivo de fuente.
5.  Envía un error si el archivo de fuente se está instalando en una carpeta que no sea FontsFolder.

## <a name="result"></a>Resultado

ICE07 publica un error si encuentra que la base de datos especifica que se debe instalar un archivo de fuente en una carpeta que no sea FontsFolder.

## <a name="example"></a>Ejemplo

IC07 publicaría el siguiente mensaje de error para el ejemplo mostrado.

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[Tabla de fuentes](font-table.md)



| Archivo\_ | FontTitle |
|--------|-----------|
| Myrtle | Tahoma    |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo   | Componente\_   |
|--------|---------------|
| Myrtle | Playera \_ de Susa |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente     | Directorio\_ |
|---------------|-------------|
| Playera \_ de Susa | SandBar     |



 

En este ejemplo, la fuente FontMosoma se asigna al archivo de fuente Deón. El archivo Quesón pertenece al componente \_ Despándalo Despándalo. En la resolución de la tabla Directory se muestra que todos los archivos que pertenecen a Beach \_ Van a instalarse en la carpeta Sandbar. Dado que no se trata de FontsFolder, ICE07 envía un mensaje de error.

Tenga en cuenta que, si el componente Desoy player pertenece realmente a la carpeta Sandbar y no a FontsFolder, es posible que la fuente Nooma no pertenezca \_ a Ninguna \_ costa. Una posible corrección del error sería incluirLooma en otro componente que se instala en el directorio FontsFolder.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



