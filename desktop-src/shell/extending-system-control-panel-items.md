---
description: Algunos de los elementos del sistema que se encuentran en Panel de control son extensibles. Para instalar una Panel de control, registre la extensión de Shell como se indica a continuación, donde name es el nombre predefinido del elemento del sistema (consulte la tabla siguiente).
title: Extender elementos de Panel de control sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8c5948ad99111dc87578dfa15c5278cf03d5918e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579601"
---
# <a name="extending-system-control-panel-items"></a>Extender elementos de Panel de control sistema

Algunos de los elementos del sistema que se encuentran en Panel de control son extensibles. Para instalar una Panel de control, registre la extensión de Shell como se indica a continuación, donde *name* es el nombre predefinido del elemento del sistema (consulte la tabla siguiente).

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

Esto es similar a la forma en que registraría una extensión para un objeto de Shell predefinido. Dado que las únicas extensiones de Shell admitidas por Panel de control son hojas de propiedades, el registro debe estar en la **subclave** \\ **Shellex PropertySheetHandlers.**




| Panel de control elemento | <em>name</em> | Observaciones | 
|--------------------|---------------|---------|
| Mostrar | Desk (Escritorio) | También admite el reemplazo de la <strong>página Escritorio.</strong><blockquote>[!Note]<br />Esto ya no se admite en Windows Vista.</blockquote><br /> | 
| Mostrar Configuración avanzado | Dispositivo | Propiedades avanzadas no específicas del software.<blockquote>[!Note]<br />Esto ya no se admite en Windows Vista.</blockquote><br /> | 
| Mostrar Configuración avanzado | Mostrar | Propiedades avanzadas específicas del hardware.<blockquote>[!Note]<br />Esto ya no se admite en Windows Vista.</blockquote><br /> | 
| Opciones de Internet | Internet | El número máximo de páginas de extensión es 18. | 
| Teclado | Teclado | El número máximo de páginas de extensión es 30. | 
| Mouse | Mouse | También admite el reemplazo de páginas estándar. El número máximo de páginas de extensión es 8. | 
| Opciones de energía | Potencia | El número máximo de páginas, incluidas las páginas estándar, es 18. | 
| Sistema | Sistema | El número máximo de páginas de extensión es 8.<blockquote>[!Note]<br />Esto ya no se admite en Windows Vista.</blockquote><br /> | 




 

El **elemento Agregar o quitar** programas del Windows XP Panel de control no es una hoja de propiedades y, por lo tanto, no se puede extender mediante los métodos aquí analizados. En su lugar, su contenido se obtiene de los publicadores de aplicaciones. Para obtener más información sobre cómo agregar contenido a Agregar o quitar programas, vea [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)e [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Panel de control elementos](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registro de Panel de control elementos](registering-control-panel-items.md)
</dt> <dt>

[Uso de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Panel de control de mensajes](message-processing.md)
</dt> <dt>

[Ejecución de Panel de control elementos](executing-control-panel-items.md)
</dt> <dt>

[Asignación de Panel de control categorías](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tareas buscables para un elemento Panel de control búsqueda](creating-searchable-task-links.md)
</dt> <dt>

[Acceso al Panel de control en modo Caja fuerte en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




