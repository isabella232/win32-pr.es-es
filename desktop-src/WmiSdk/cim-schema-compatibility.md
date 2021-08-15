---
description: Compatibilidad de esquemas CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Compatibilidad de esquemas CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d87f1e40a52998f3a53a9b06f0572d8916b4a53663354ca5ffde67beaeed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319791"
---
# <a name="cim-schema-compatibility"></a>Compatibilidad de esquemas CIM

Un componente clave de la infraestructura Windows Instrumental de administración de recursos (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema. El modelo se ajusta a un estándar mantenido por el Grupo de tareas de administración de escritorio[(DMTF)](https://www.dmtf.org/standards/wsman)y se conoce como Modelo de información común (CIM). El esquema CIM proporciona un único mecanismo de descripción de datos para los datos que proporcionan.

A partir Windows 7, WMI es compatible con el esquema CIM versión 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ). Los usuarios ahora pueden compilar un esquema definido por DMTF en un Windows equipo.

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a>Ventajas de la compatibilidad con el esquema CIM versión 2.17.1

-   Cuando un usuario descarga los archivos CIM Schema version 2.17.1 o DMTF MOF, se pueden compilar correctamente en el equipo Windows destino.
-   La versión 2.17.1 del esquema CIM agregó compatibilidad con BIOS, impresoras, mensajes estándar, estado del sistema operativo, paradigmas modernos de administración de energía, virtualización y seguridad.
-   La versión 2.1.7.1 del esquema CIM ofrece compatibilidad con perfiles adicionales. Para obtener más información, vea [Cross Namespace Association Traversal (Recorrido de asociación entre espacios de nombres).](cross-namespace-association-traversal.md)

 

 



