---
description: Managed Object Format (MOF) es el lenguaje que se usa para describir las clases de Modelo de información común (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: Managed Object Format (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697540"
---
# <a name="managed-object-format-mof"></a>Managed Object Format (MOF)

Managed Object Format (MOF) es el lenguaje que se usa para describir las clases de [*modelo de información común (CIM)*](gloss-c.md) .

La manera recomendada para que los proveedores de WMI implementen nuevas clases WMI es en archivos MOF que se compilan mediante [**Mofcomp.exe**](mofcomp.md) en el [*repositorio WMI*](gloss-w.md). También es posible crear y manipular clases CIM e instancias mediante la [API com para WMI](com-api-for-wmi.md).

Un proveedor WMI normalmente consta de un archivo MOF, que define los datos y las clases de eventos para los que el proveedor devuelve datos, y un archivo DLL que contiene el código que proporciona los datos. Para obtener más información, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).

Las aplicaciones y scripts de cliente WMI pueden consultar instancias de clases MOF de proveedor o suscribirse para recibir notificaciones de eventos.

Puede realizar las siguientes tareas con MOF:

-   [Compilar archivos MOF](compiling-mof-files.md)
-   [Crear una clase](creating-a-class.md)
-   [Crear una instancia](creating-an-instance.md)
-   [Crear un método](creating-a-method.md)
-   [Adición de un calificador](adding-a-qualifier.md)
-   [Crear un comentario](creating-a-comment.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 



