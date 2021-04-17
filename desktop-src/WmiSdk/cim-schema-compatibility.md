---
description: Compatibilidad con esquemas CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Compatibilidad con esquemas CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df559469ef6a8284b51951dc365bad6c302ca865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716701"
---
# <a name="cim-schema-compatibility"></a>Compatibilidad con esquemas CIM

Un componente clave de la infraestructura de Instrumental de administración de Windows (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema. El modelo se ajusta a un estándar mantenido por el equipo de tareas de administración de escritorio ([DMTF](https://www.dmtf.org/standards/wsman)) y se conoce como modelo de información común (CIM). El esquema CIM proporciona un único mecanismo de descripción de datos para cualquier dato que proporcionen.

A partir de Windows 7, WMI es compatible con la versión del esquema CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ). Los usuarios ahora pueden compilar un esquema definido por DMTF en un equipo Windows.

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a>Ventajas de la compatibilidad con la versión de esquema CIM 2.17.1

-   Cuando un usuario descarga archivos MOF de la versión de esquema CIM 2.17.1 o de DMTF, se pueden compilar correctamente en el equipo de Windows de destino.
-   La versión del esquema CIM 2.17.1 agregó compatibilidad con BIOS, impresoras, mensajes estándar, estado del sistema operativo, paradigmas modernos de administración de energía, virtualización y seguridad.
-   La versión del esquema CIM 2.1.7.1 ofrece compatibilidad adicional con el perfil. Para obtener más información, vea cruce seguro de la [asociación entre espacios de nombres](cross-namespace-association-traversal.md)

 

 



