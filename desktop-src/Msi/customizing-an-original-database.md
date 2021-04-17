---
description: Realice una copia del paquete de instalación de Windows Installer de ejemplo MNP2000.msi y cambie el nombre de esta MNP2000t.msi de copia.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Personalización de una base de datos original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3222ebce146e891c7b16c70eb78f0f26b95727c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666586"
---
# <a name="customizing-an-original-database"></a>Personalización de una base de datos original

Realice una copia del paquete de instalación de Windows Installer de ejemplo MNP2000.msi y cambie el nombre de esta MNP2000t.msi de copia. En los pasos siguientes personalizará este archivo con un editor de tablas de base de datos como orca, que se proporciona con el SDK u otro editor de bases de datos.

Incluya el nuevo archivo de recursos para la lista de teléfonos, Phone.txt, en la carpeta del Bloc de notas con los otros archivos de origen.



| Archivo      | Descripción                             | Ruta de acceso al origen                 | Ruta de acceso al destino                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Un recurso para la característica de lista de teléfonos \_ . | C: \\phone.txt del Bloc de notas de ejemplo \\ \\ | \[phone.txt en el \] \\ \_ estacionamiento rojo \\ |



 

Utilice el editor de base de datos para agregar un registro a la [tabla de archivos](file-table.md) de MNP2000t.msi del nuevo archivo.

[Tabla de archivos](file-table.md)



| Archivo      | Componente\_ | FileName  | FileSize | Versión | Idioma | Atributos | Secuencia |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Teléfono       | Phone.txt | 1000     |         |          | 0          | 1        |



 

Como se explica en la sección: [usar transformaciones para agregar recursos](using-transforms-to-add-resources.md), la transformación debe agregar uno o varios componentes nuevos a la base de datos de instalación para que contenga la nueva característica de lista de teléfonos. Utilice el editor de base de datos para agregar el Registro siguiente a la [tabla de componentes](component-table.md) de MNP2000t.msi.

El componente de teléfono debe identificarse con un [GUID](guid.md)de identificador de componente único. Si está reproduciendo el ejemplo, no vuelva a usar el mismo GUID de ID. de componente que en la tabla siguiente. En su lugar, use una utilidad como Guidgen.exe para generar un nuevo GUID. Asegúrese de usar una cadena de GUID coherente con el tipo de datos Windows Installer [GUID](guid.md) .

[Tabla de componentes](component-table.md)



| Componente | ComponentId                            | Directorio\_ | Atributos | Condición | Rutas   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Teléfono     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Utilice el editor de base de datos para modificar los datos de la [tabla de características](feature-table.md) de MNP2000t.msi. Escriba 0 en la columna LEVEL del registro de características de la puerta. Esto deshabilita la característica de puerta y sus características secundarias, y oculta estas características de la interfaz de usuario. Tenga en cuenta que, dado que la propiedad [**INSTALLLEVEL**](installlevel.md) está establecida en 3 en la [tabla de propiedades](property-table.md), el instalador no instala las características con un nivel de 0. Agregue un registro para la nueva característica de lista de teléfonos \_ .

[Tabla de características](feature-table.md)



| Característica     | Característica \_ principal | Title         | Descripción                | Pantalla | Nivel | Directorio\_ | Atributos |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Cultura        |                 | Cultura          | Arts Events en el Parque rojo.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baloncesto    | Deporte           | Baloncesto      | Juegos de béisbol             | 17      | 3     | SPORTDIR    | 32         |
| Concierto     | Cultura            | Concierto       | Eventos de concierto en el Parque rojo | 21      | 3     | ARTSDIR     | 2          |
| Dance       | Cultura            | Dance         | Eventos de baile en el Parque rojo   | 23      | 3     | ARTSDIR     | 2          |
| Balón    | Deporte           | Balón      | Juegos de fútbol             | 19      | 3     | SPORTDIR    | 2          |
| Canaliza        |                 | Canaliza          | Admisiones del parque rojo      | 6       | 0     | NOTEPADDIR  | 0          |
| Ayuda        | Bloc de notas         | Ayuda          | Archivo de ayuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January     | Canaliza            | January       | Admisiones de enero         | 10      | 3     | MONDIR      | 2          |
| NewYears    | January         | Día de los años nuevos | Nuevas Admisiones del día de los años   | 11      | 3     | HOLDIR      | 2          |
| Bloc de notas     |                 | Bloc de notas       | Editor del Bloc de notas             | 1       | 3     | NOTEPADDIR  | 0          |
| Léame      | Bloc de notas         | Léame        | Archivo Léame                | 3       | 3     | NOTEPADDIR  | 0          |
| Deporte       |                 | Eventos deportivos  | Acontecimientos deportivos en el Parque rojo   | 14      | 3     | NOTEPADDIR  | 0          |
| Lista de teléfonos \_ |                 | Lista telefónica    | Lista telefónica                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Agregue el Registro siguiente a la [tabla FeatureComponents](featurecomponents-table.md) de MNP2000t.msi.

[Tabla FeatureComponents](featurecomponents-table.md)



| Característica\_   | Componente\_ |
|-------------|-------------|
| Lista de teléfonos \_ | Teléfono       |



 

Agregue un nuevo registro en la [tabla de accesos directos](shortcut-table.md) para crear un acceso directo a la característica de lista de teléfonos \_ .

[Tabla de acceso directo](shortcut-table.md)



| Acceso directo | Directorio\_ | Nombre      | Componente\_ | Destino          | Argumentos | Descripción | Tecla de acceso rápido | Icono\_ | IconIndex | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| sPhone   | MENUDIR     | Phone.txt | Teléfono       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Continuar](generating-a-customization-transform.md)

 

 



