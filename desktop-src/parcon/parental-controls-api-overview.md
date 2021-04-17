---
description: Información general sobre la API de controles parentales
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Información general sobre la API de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716999"
---
# <a name="parental-controls-api-overview"></a><span data-ttu-id="85b0f-103">Información general sobre la API de controles parentales</span><span class="sxs-lookup"><span data-stu-id="85b0f-103">Parental Controls API Overview</span></span>

<span data-ttu-id="85b0f-104">Las API que se usan para controles parentales exponen la Directiva y las restricciones en el cuadro y la funcionalidad de registro.</span><span class="sxs-lookup"><span data-stu-id="85b0f-104">APIs used for Parental Controls expose the policy and in-box restrictions settings, and logging functionality.</span></span>

## <a name="settings"></a><span data-ttu-id="85b0f-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="85b0f-105">Settings</span></span>

<span data-ttu-id="85b0f-106">Se proporcionan dos API públicas:</span><span class="sxs-lookup"><span data-stu-id="85b0f-106">Two public APIs are provided:</span></span>

-   <span data-ttu-id="85b0f-107">Una API de cumplimiento mínimo basada en COM (denominada API de cumplimiento) principalmente para las aplicaciones para determinar si se debe activar el registro.</span><span class="sxs-lookup"><span data-stu-id="85b0f-107">A lightweight COM-based minimum compliance API (called the Compliance API) primarily for applications to determine whether logging should be turned on.</span></span> <span data-ttu-id="85b0f-108">Además, se proporcionan métodos simples para:</span><span class="sxs-lookup"><span data-stu-id="85b0f-108">In addition, simple methods are provided for:</span></span>
    -   <span data-ttu-id="85b0f-109">Recuperación del estado de restricciones para restricciones Web, límites de tiempo, restricciones de juegos y restricciones de aplicación.</span><span class="sxs-lookup"><span data-stu-id="85b0f-109">Retrieving the restrictions state for web restrictions, time limits, games restrictions, and application restrictions.</span></span>
    -   <span data-ttu-id="85b0f-110">Recuperando el identificador del filtro de contenido Web activo.</span><span class="sxs-lookup"><span data-stu-id="85b0f-110">Retrieving the ID of the active Web content filter.</span></span>
    -   <span data-ttu-id="85b0f-111">Determinar si se deben mostrar los elementos de la interfaz de usuario del proveedor, de manera coherente con la ocultación en el cuadro cuando se une a un dominio.</span><span class="sxs-lookup"><span data-stu-id="85b0f-111">Determining whether vendor user interface elements should be shown, in a manner consistent with the in-box hiding when joined to a domain.</span></span>
    -   <span data-ttu-id="85b0f-112">Recuperar la última vez que se ha cambiado un valor de configuración para un usuario.</span><span class="sxs-lookup"><span data-stu-id="85b0f-112">Retrieving the last time a setting has been changed for a user.</span></span>
    -   <span data-ttu-id="85b0f-113">Recuperación de si se debe bloquear la descarga de archivos basados en el explorador o en el explorador para un usuario, así como la capacidad de solicitar una dirección URL que permita específicamente el filtro de contenido web para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="85b0f-113">Retrieving whether browser-based or browser-like file downloads need to be blocked for a user, and the ability to request a URL to be specifically allowed by the Web Content Filter for that user.</span></span>
    -   <span data-ttu-id="85b0f-114">Determinar si un juego determinado está bloqueado para un usuario.</span><span class="sxs-lookup"><span data-stu-id="85b0f-114">Determining whether a given game is blocked for a user.</span></span>
-   <span data-ttu-id="85b0f-115">Acceso de API de Instrumental de administración de Windows (WMI) a un espacio de nombres de controles parentales para el acceso de lectura y escritura completo a todos los valores expuestos.</span><span class="sxs-lookup"><span data-stu-id="85b0f-115">Windows Management Instrumentation (WMI) API access to a Parental Controls namespace for full write and read access to all exposed settings.</span></span> <span data-ttu-id="85b0f-116">El control parental implementa un proveedor de WMI para administrar los permisos de lectura y escritura en el almacén de configuración subyacente con el cumplimiento adecuado de los privilegios para administradores y usuarios controlados.</span><span class="sxs-lookup"><span data-stu-id="85b0f-116">Parental Controls deploys a WMI Provider to manage read/write permissions to the underlying settings store with proper enforcement of privileges for administrators and controlled users.</span></span>

<span data-ttu-id="85b0f-117">Se solicita a los ISV que usen la API de cumplimiento y la API de WMI según sea necesario para controlar las restricciones según sea necesario para la seguridad secundaria basada en la funcionalidad de la aplicación o la solución.</span><span class="sxs-lookup"><span data-stu-id="85b0f-117">ISVs are requested to use the Compliance API, and the WMI API as necessary, to control restrictions as appropriate for child safety based on the functionality of the application or solution.</span></span>

## <a name="logging"></a><span data-ttu-id="85b0f-118">Registro</span><span class="sxs-lookup"><span data-stu-id="85b0f-118">Logging</span></span>

-   <span data-ttu-id="85b0f-119">Las API de consumo y publicación de eventos estándar de Windows se usan para la supervisión de la actividad de controles parentales.</span><span class="sxs-lookup"><span data-stu-id="85b0f-119">Windows standard event publishing and consuming APIs are used for Parental Controls activity monitoring.</span></span> <span data-ttu-id="85b0f-120">El sistema de informes y seguimiento de eventos de Windows Vista ha mejorado el rendimiento respecto a la funcionalidad anterior de seguimiento de eventos para Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="85b0f-120">The Windows Vista Event Reporting and Tracing system has improved performance over previous Event Tracing for Windows (ETW) functionality.</span></span> <span data-ttu-id="85b0f-121">Controles parentales define un canal único para sus datos en ETW.</span><span class="sxs-lookup"><span data-stu-id="85b0f-121">Parental Controls defines a unique channel for its data in ETW.</span></span>
-   <span data-ttu-id="85b0f-122">Se solicita a los ISV que usen la API de publicación de eventos para registrar la actividad de los usuarios según se especifica en la sección uso de las API de controles parentales.</span><span class="sxs-lookup"><span data-stu-id="85b0f-122">ISVs are requested to use the event publishing API to log user activity as specified in the Using Parental Controls APIs section.</span></span>

 

 



