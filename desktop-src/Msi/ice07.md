---
description: ICE07 valida que el paquete de instalación especifica que las fuentes se instalan en FontsFolder. Si una fuente se instala en una carpeta que no sea la FontsFolder, el instalador crea un acceso directo en lugar de instalar realmente la fuente.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652821"
---
# <a name="ice07"></a>ICE07

ICE07 valida que el paquete de instalación especifica que las fuentes se instalan en FontsFolder. Si una fuente se instala en una carpeta que no sea la FontsFolder, el instalador crea un acceso directo en lugar de instalar realmente la fuente.

La acción personalizada ICE07 realiza lo siguiente para cada fuente de la [tabla de fuentes](font-table.md).

1.  Busca el archivo de fuente al que pertenece cada título de fuente mediante la [tabla de fuentes](font-table.md).
2.  Consulta la \_ columna componente de la [tabla de archivos](file-table.md) del componente que controla cada archivo.
3.  Consulta la \_ columna directorio de la [tabla de componentes](component-table.md) para obtener una clave en la tabla de directorios.
4.  Resuelve la tabla de [directorio](directory-table.md) para determinar el nombre de la carpeta en la que el instalador va a instalar el archivo de fuente.
5.  Envía un error si el archivo de fuente se instala en una carpeta distinta de FontsFolder.

## <a name="result"></a>Resultado

ICE07 publica un error si detecta que la base de datos especifica que un archivo de fuente se instala en una carpeta distinta de la FontsFolder.

## <a name="example"></a>Ejemplo

IC07 publicaría el mensaje de error siguiente para el ejemplo mostrado.

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
| Myrtle | Myrtle \_ Beach |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente     | Directorio\_ |
|---------------|-------------|
| Myrtle \_ Beach | SandBar     |



 

En este ejemplo, la fuente Tahoma se asigna al archivo de fuente Myrtle. El archivo Myrtle pertenece al componente Myrtle \_ Beach. La resolución de la tabla de directorios muestra que todos los archivos que pertenecen a Myrtle \_ Beach se van a instalar en la carpeta Sandbar. Como no se FontsFolder, ICE07 envía un mensaje de error.

Tenga en cuenta que si el componente Myrtle \_ Beach realmente pertenece a la carpeta Sandbar, y no al FontsFolder, es posible que la fuente Tahoma no pertenezca a Myrtle \_ Beach. Una posible solución para el error sería incluir Tahoma en otro componente que se instala en el directorio FontsFolder

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



