---
description: A Windows XP, Panel de control categorización de Panel de control elementos. Los elementos se registran para que aparezcan en una o varias categorías. No se pueden crear nuevas categorías.
title: Asignación de Panel de control categorías
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b6785a786bfe80f5a5b13bc5e9dfbe39507a2c9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478491"
---
# <a name="assigning-control-panel-categories"></a>Asignación de Panel de control categorías

A Windows XP, Panel de control categorización de Panel de control elementos. Los elementos se registran para que aparezcan en una o varias categorías. No se pueden crear nuevas categorías.

Para registrar un elemento Panel de control en una o varias categorías, agregue valores como se explica en la sección Registro de elementos ejecutables de [Panel de control](registering-control-panel-items.md) o Registro de elementos dll [Panel de control](registering-control-panel-items.md) de Registro de elementos Panel de control [,](registering-control-panel-items.md)según corresponda.




| Id. de categoría | Nombre de categoría (Windows 7) | Nombre de categoría (Windows Vista) | Nombre de categoría (Windows XP) | 
|-------------|---------------------------|-------------------------------|----------------------------|
| 0 | "All Panel de control Items" | "Opciones adicionales"<blockquote>[!Note]<br />Cualquier Panel de control elemento que no especifique un identificador de categoría aparece en esta categoría.</blockquote><br /> | "Other Panel de control Options"<blockquote>[!Note]<br />Cualquier Panel de control elemento que no especifique un identificador de categoría aparece en esta categoría.</blockquote><br /> | 
| 1 | "Apariencia y personalización" | "Apariencia y personalización" | "Apariencia y temas" | 
| 2 | "Hardware y sonido" | "Hardware y sonido" | "Impresoras y otro hardware" | 
| 3 | "Red e Internet" | "Red e Internet" | "Conexiones de red e Internet" | 
| 4 | Ya no se usa. Cualquier elemento que se agrega solo a la categoría 4 aparece en la categoría 2 (Hardware y sonido). | Ya no se usa. Cualquier elemento que se agrega solo a la categoría 4 aparece en la categoría 2 (Hardware y sonido). | "Sonidos, voz y dispositivos de audio" | 
| 5 | "Sistema y seguridad" | "Sistema y mantenimiento" | "Rendimiento y mantenimiento" | 
| 6 | "Reloj, idioma y región" | "Reloj, idioma y región" | "Fecha, hora, idioma y opciones regionales" | 
| 7 | "Accesibilidad" | "Accesibilidad" | "Opciones de accesibilidad" | 
| 8 | "Programas" | "Programas" | "Agregar o quitar programas" | 
| 9 | "Cuentas de usuario"<blockquote>[!Note]<br />Cuando no está conectado a un dominio, se denomina "Cuentas de usuario y seguridad de familia".</blockquote><br /> | "Cuentas de usuario"<blockquote>[!Note]<br />Cuando no está conectado a un dominio, se denomina "Cuentas de usuario y seguridad de familia".</blockquote><br /> | "Cuentas de usuario" | 
| 10 | Ya no se usa. Los elementos registrados en esta categoría aparecen en la categoría 5 (Sistema y seguridad). | "Security" | "Security Center"<blockquote>[!Note]<br />Solo está disponible en Windows XP Service Pack 2 (SP2) o posterior.</blockquote><br /> | 
| 11 | Ya no se usa. Los elementos registrados en esta categoría aparecen en la categoría 0 (Todos Panel de control elementos). | "PC móvil"<blockquote>[!Note]<br />Esta categoría solo es visible en equipos móviles.</blockquote><br /> | No se utiliza. | 




 

En Windows XP, las categorías **Agregar** o  quitar programas y cuentas de usuario funcionan de forma ligeramente diferente a otras categorías de Panel de control. Cuando se agregan uno o varios elementos a una de estas dos categorías, el vínculo asociado en Panel de control abre una página de categorías. Los elementos registrados aparecen en la parte inferior de la página bajo el encabezado "o Elegir un Panel de control". Cuando no se registra ningún elemento para una de estas categorías, el vínculo asociado de Panel de control invoca directamente el elemento Windows estándar para esa categoría. En Windows Vista y versiones posteriores, la categoría **Programas** y la categoría **Cuentas** de usuario no tienen esta propiedad.

La **Security Center,** disponible solo en Windows XP SP2, también es algo no estándar. Al hacer clic en esta **categoría, se Security Center** página en una nueva ventana. Los elementos registrados **Security Center** aparecen en la parte inferior de esa página bajo el encabezado **Administrar la configuración de seguridad para:**. Al hacer clic en un icono, se Panel de control elemento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Panel de control de datos](control-panel-applications.md)
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

[Extender elementos de Panel de control sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Crear vínculos de tareas que se pueden buscar para un elemento Panel de control búsqueda](creating-searchable-task-links.md)
</dt> <dt>

[Acceso al Panel de control en modo Caja fuerte en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




