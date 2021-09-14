---
description: En el ejemplo siguiente se muestra cómo iniciar un archivo HTML al final de una instalación.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Usar una acción personalizada para iniciar un archivo instalado al final de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069589"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a>Usar una acción personalizada para iniciar un archivo instalado al final de la instalación

En el ejemplo siguiente se muestra cómo iniciar un archivo HTML al final de una instalación. El instalador instala el componente que contiene el archivo y, a continuación, publica un evento de control al final de la instalación para ejecutar una acción personalizada que abre el archivo. Este enfoque se puede usar para iniciar un tutorial de ayuda al final de la primera instalación de una aplicación.

El ejemplo debe cumplir las especificaciones siguientes.

-   El instalador ejecuta la acción personalizada solo si se usa el [*nivel de*](f-gly.md) interfaz de usuario completo para instalar una aplicación.
-   El instalador ejecuta la acción personalizada solo si el componente que contiene el archivo HTML está instalado para ejecutarse localmente en el equipo.
-   La acción personalizada solo se ejecuta en la primera instalación de la aplicación.
-   La instalación no produce un error si se produce un error en la acción personalizada.

El ejemplo incluye un componente hipotético denominado Tutorial que controla al menos un recurso, un archivo denominado tutorial.htm. El identificador de este archivo en la columna Archivo de la tabla Archivo es Tutorial. En la siguiente explicación se da por supuesto que ya ha creado los recursos necesarios para el Tutorial y que ha realizado todas las entradas necesarias en las tablas [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md)y [FeatureComponents](featurecomponents-table.md) para instalar este componente. Para obtener más información, vea [Un ejemplo de instalación](an-installation-example.md).

Los temas siguientes contienen información sobre cómo crear las acciones personalizadas necesarias y agregarlas a un paquete de instalación.

-   [Creación de la acción personalizada Launch](authoring-the-launch-custom-action.md)
-   [Agregar Launch a las tablas CustomAction y Binary](adding-launch-to-the-customaction-and-binary-tables.md)
-   [Agregar un evento de control al final de la instalación para ejecutar el inicio](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



