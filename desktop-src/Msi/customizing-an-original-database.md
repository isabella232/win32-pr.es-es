---
description: Realice una copia del paquete de instalación del instalador Windows ejemplo y MNP2000.msi cambiar el nombre de esta copia MNP2000t.msi.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Personalización de una base de datos original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f02f176bb24b1792d9184ebc662a45c9dbfdb8df385b3fb481967c9c8a099a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075045"
---
# <a name="customizing-an-original-database"></a>Personalización de una base de datos original

Realice una copia del paquete de instalación del instalador Windows ejemplo y MNP2000.msi cambiar el nombre de esta copia MNP2000t.msi. En los pasos siguientes personalizará este archivo mediante un editor de tablas de base de datos como Orca, que se proporciona con el SDK, u otro editor de bases de datos.

Incluya el nuevo archivo de recursos para la lista de teléfonos, Phone.txt, en la carpeta Bloc de notas con los demás archivos de origen.



| Archivo      | Descripción                             | Ruta de acceso al origen                 | Ruta de acceso al destino                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Un recurso para la característica Teléfono \_ list. | C: \\ Ejemplo \\ Bloc de notas \\phone.txt | \[ProgramFilesFolder \] \\ Red Park \_ \\phone.txt |



 

Use el editor de base de datos para agregar un registro a la [tabla File](file-table.md) MNP2000t.msi para el nuevo archivo.

[Tabla de archivos](file-table.md)



| Archivo      | Componente\_ | FileName  | FileSize | Versión | Lenguaje | Atributos | Secuencia |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Teléfono       | Phone.txt | 1000     |         |          | 0          | 1        |



 

Como se explica en la [sección:](using-transforms-to-add-resources.md)Uso de transformaciones para agregar recursos, la transformación debe agregar uno o varios componentes nuevos a la base de datos de instalación para que contenga la nueva característica de lista de teléfonos. Use el editor de bases de datos para agregar el registro siguiente a la [tabla Component de](component-table.md) MNP2000t.msi.

El Teléfono componente debe identificarse con un GUID de identificador de [componente único.](guid.md) Si va a reproducir el ejemplo, no reutilice el mismo GUID de identificador de componente que en la tabla siguiente. En su lugar, use una utilidad como Guidgen.exe para generar un nuevo GUID. Asegúrese de usar una cadena GUID coherente con el tipo de Windows [guid del](guid.md) instalador.

[Tabla de componentes](component-table.md)



| Componente | Componentid                            | Directorio\_ | Atributos | Condición | Ruta de acceso de clave   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Teléfono     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Use el editor de bases de datos para modificar los datos de la [tabla Característica](feature-table.md) de MNP2000t.msi. Escriba 0 en la columna Nivel del registro de características de puerta. Esto deshabilita la característica Puerta y sus características secundarias y oculta estas características de la interfaz de usuario. Tenga en cuenta que, dado que [**la propiedad INSTALLLEVEL**](installlevel.md) está establecida en 3 en la tabla [Property](property-table.md), el instalador no instala características con un nivel de 0. Agregue un registro para la nueva característica Teléfono \_ list.

[Tabla de características](feature-table.md)



| Característica     | Elemento \_ primario de la característica | Título         | Descripción                | Mostrar | Nivel | Directorio\_ | Atributos |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Artes        |                 | Artes          | Eventos de eventos en Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Béisbol    | Deporte           | Béisbol      | Juegos de béisbol             | 17      | 3     | SPORTDIR    | 32         |
| Concierto     | Artes            | Concierto       | Eventos de un concierto en Red Park | 21      | 3     | NOCIONESDIR     | 2          |
| Baile       | Artes            | Baile         | Eventos de música en Red Park   | 23      | 3     | NOCIONESDIR     | 2          |
| Fútbol    | Deporte           | Fútbol      | Partidos de fútbol             | 19      | 3     | SPORTDIR    | 2          |
| Puerta        |                 | Puerta          | Admisiones de Red Park      | 6       | 0     | NOTEPADDIR  | 0          |
| Ayuda        | Bloc de notas         | Ayuda          | Archivo de ayuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January     | Puerta            | January       | Admisiones de enero         | 10      | 3     | MONDIR      | 2          |
| NewYears    | January         | Día de los nuevos años | Admisiones de año nuevo   | 11      | 3     | HOLDIR      | 2          |
| Bloc de notas     |                 | Bloc de notas       | Bloc de notas Editor             | 1       | 3     | NOTEPADDIR  | 0          |
| Léame      | Bloc de notas         | Léame        | Archivo Léame                | 3       | 3     | NOTEPADDIR  | 0          |
| Deporte       |                 | Eventos deportivos  | Eventos deportivos en Red Park   | 14      | 3     | NOTEPADDIR  | 0          |
| \_Teléfono Lista |                 | Lista telefónica    | Lista telefónica                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Agregue el registro siguiente a la [tabla FeatureComponents](featurecomponents-table.md) de MNP2000t.msi.

[Tabla FeatureComponents](featurecomponents-table.md)



| Característica\_   | Componente\_ |
|-------------|-------------|
| \_Teléfono Lista | Teléfono       |



 

Agregue un nuevo registro en la tabla [Acceso directo](shortcut-table.md) para crear un acceso directo a la característica Teléfono lista \_ de accesos directos.

[Tabla de métodos abreviados](shortcut-table.md)



| Acceso directo | Directorio\_ | Nombre      | Componente\_ | Destino          | Argumentos | Descripción | Tecla de acceso rápido | Icono\_ | IconIndex | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| sPhone   | MENUDIR     | Phone.txt | Teléfono       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Continuar](generating-a-customization-transform.md)

 

 



