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
# <a name="cim-schema-compatibility"></a><span data-ttu-id="0fc4d-103">Compatibilidad con esquemas CIM</span><span class="sxs-lookup"><span data-stu-id="0fc4d-103">CIM Schema Compatibility</span></span>

<span data-ttu-id="0fc4d-104">Un componente clave de la infraestructura de Instrumental de administración de Windows (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema.</span><span class="sxs-lookup"><span data-stu-id="0fc4d-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="0fc4d-105">El modelo se ajusta a un estándar mantenido por el equipo de tareas de administración de escritorio ([DMTF](https://www.dmtf.org/standards/wsman)) y se conoce como modelo de información común (CIM).</span><span class="sxs-lookup"><span data-stu-id="0fc4d-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="0fc4d-106">El esquema CIM proporciona un único mecanismo de descripción de datos para cualquier dato que proporcionen.</span><span class="sxs-lookup"><span data-stu-id="0fc4d-106">The CIM schema provides a single data description mechanism for any data that they provide.</span></span>

<span data-ttu-id="0fc4d-107">A partir de Windows 7, WMI es compatible con la versión del esquema CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ).</span><span class="sxs-lookup"><span data-stu-id="0fc4d-107">Starting in Windows 7, WMI is compatible with the CIM Schema version 2.17.1 ([https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171)).</span></span> <span data-ttu-id="0fc4d-108">Los usuarios ahora pueden compilar un esquema definido por DMTF en un equipo Windows.</span><span class="sxs-lookup"><span data-stu-id="0fc4d-108">Users can now compile a DMTF defined schema on a Windows computer.</span></span>

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a><span data-ttu-id="0fc4d-109">Ventajas de la compatibilidad con la versión de esquema CIM 2.17.1</span><span class="sxs-lookup"><span data-stu-id="0fc4d-109">Benefits of CIM Schema version 2.17.1 compatibility</span></span>

-   <span data-ttu-id="0fc4d-110">Cuando un usuario descarga archivos MOF de la versión de esquema CIM 2.17.1 o de DMTF, se pueden compilar correctamente en el equipo de Windows de destino.</span><span class="sxs-lookup"><span data-stu-id="0fc4d-110">When a user downloads CIM Schema version 2.17.1 or DMTF MOF files, they can be successfully compiled on the target Windows computer.</span></span>
-   <span data-ttu-id="0fc4d-111">La versión del esquema CIM 2.17.1 agregó compatibilidad con BIOS, impresoras, mensajes estándar, estado del sistema operativo, paradigmas modernos de administración de energía, virtualización y seguridad.</span><span class="sxs-lookup"><span data-stu-id="0fc4d-111">The CIM Schema version 2.17.1 added support for BIOS, printers, standard messages, operating system state, modern power management paradigms, virtualization and security.</span></span>
-   <span data-ttu-id="0fc4d-112">La versión del esquema CIM 2.1.7.1 ofrece compatibilidad adicional con el perfil.</span><span class="sxs-lookup"><span data-stu-id="0fc4d-112">CIM Schema version 2.1.7.1 offers additional profile support.</span></span> <span data-ttu-id="0fc4d-113">Para obtener más información, vea cruce seguro de la [asociación entre espacios de nombres](cross-namespace-association-traversal.md)</span><span class="sxs-lookup"><span data-stu-id="0fc4d-113">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md)</span></span>

 

 



