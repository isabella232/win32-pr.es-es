---
description: Algunos de los elementos del sistema que se encuentran en el panel de control son extensibles. Para instalar una extensión del panel de control, registre la extensión de shell como se indica a continuación, donde nombre es el nombre predefinido del elemento del sistema (vea la tabla siguiente).
title: Extender elementos del panel de control del sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997301"
---
# <a name="extending-system-control-panel-items"></a>Extender elementos del panel de control del sistema

Algunos de los elementos del sistema que se encuentran en el panel de control son extensibles. Para instalar una extensión del panel de control, registre la extensión de shell como se indica a continuación, donde *nombre* es el nombre predefinido del elemento del sistema (vea la tabla siguiente).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

Esto es similar a la manera en que registraría una extensión para un objeto de Shell predefinido. Dado que las únicas extensiones de Shell que admiten los elementos del panel de control son hojas de propiedades, el registro debe estar bajo la subclave **shellex** \\ **PropertySheetHandlers** .



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento del panel de control</th>
<th><em>name</em></th>
<th>Observaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pantalla</td>
<td>Desk (Escritorio)</td>
<td>También admite el reemplazo de la página del <strong>escritorio</strong> .
<blockquote>
[!Note]<br />
Ya no se admite en Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Configuración de pantalla avanzada</td>
<td>Dispositivo</td>
<td>Propiedades avanzadas no específicas del hardware.
<blockquote>
[!Note]<br />
Ya no se admite en Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Configuración de pantalla avanzada</td>
<td>Pantalla</td>
<td>Propiedades avanzadas específicas del hardware.
<blockquote>
[!Note]<br />
Ya no se admite en Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Opciones de Internet</td>
<td>Internet</td>
<td>El número máximo de páginas de extensión es 18.</td>
</tr>
<tr class="odd">
<td>Teclado</td>
<td>Teclado</td>
<td>El número máximo de páginas de extensión es 30.</td>
</tr>
<tr class="even">
<td>Mouse</td>
<td>Mouse</td>
<td>También admite la sustitución de páginas estándar. El número máximo de páginas de extensión es 8.</td>
</tr>
<tr class="odd">
<td>Opciones de energía</td>
<td>Power</td>
<td>El número máximo de páginas, incluidas las páginas estándar, es 18.</td>
</tr>
<tr class="even">
<td>Sistema</td>
<td>Sistema</td>
<td>El número máximo de páginas de extensión es 8.
<blockquote>
[!Note]<br />
Ya no se admite en Windows Vista.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

El elemento **Agregar o quitar programas** del panel de control de Windows XP no es una hoja de propiedades y, por tanto, no se puede ampliar con los métodos descritos aquí. En su lugar, su contenido se obtiene de los publicadores de aplicaciones. Para obtener más información sobre cómo agregar contenido para **Agregar o quitar programas**, consulte [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)y [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Usar CPLApplet](using-cplapplet.md)
</dt> <dt>

[Procesamiento de mensajes del panel de control](message-processing.md)
</dt> <dt>

[Ejecutar elementos del panel de control](executing-control-panel-items.md)
</dt> <dt>

[Asignar categorías del panel de control](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md)
</dt> <dt>

[Acceder al panel de control en modo seguro en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




