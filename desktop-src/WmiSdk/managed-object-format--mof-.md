---
description: Managed Object Format (MOF) es el lenguaje que se usa para describir las Modelo de información común (CIM).
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
ms.openlocfilehash: ac36bd89979d6cf0de0a4d574a47a6ce7060f90e5577402eba77aa2de42bbedb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131187"
---
# <a name="managed-object-format-mof"></a>Managed Object Format (MOF)

Managed Object Format (MOF) es el lenguaje que se usa para describir las [*Modelo de información común (CIM).*](gloss-c.md)

La manera recomendada para que los proveedores wmi implementen nuevas clases WMI es en archivos MOF que se compilanMofcomp.exe [**en**](mofcomp.md) el [*repositorio WMI*](gloss-w.md). También es posible crear y manipular instancias y clases CIM mediante la [API COM para WMI.](com-api-for-wmi.md)

Normalmente, un proveedor WMI consta de un archivo MOF, que define los datos y las clases de eventos para los que el proveedor devuelve datos, y un archivo DLL que contiene el código que proporciona los datos. Para obtener más información, vea [Proporcionar datos a WMI.](providing-data-to-wmi.md)

Las aplicaciones y scripts de cliente WMI pueden consultar instancias de clases MOF del proveedor o suscribirse para recibir notificaciones de eventos.

Puede realizar las siguientes tareas con MOF:

-   [Compilación de archivos MOF](compiling-mof-files.md)
-   [Crear una clase](creating-a-class.md)
-   [Creación de una instancia](creating-an-instance.md)
-   [Crear un método](creating-a-method.md)
-   [Agregar un calificador](adding-a-qualifier.md)
-   [Crear un comentario](creating-a-comment.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 



