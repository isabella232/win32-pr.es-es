---
description: Uso de las API de controles parentales
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Uso de las API de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720523"
---
# <a name="using-parental-controls-apis"></a><span data-ttu-id="5535d-103">Uso de las API de controles parentales</span><span class="sxs-lookup"><span data-stu-id="5535d-103">Using Parental Controls APIs</span></span>

## <a name="api-selection"></a><span data-ttu-id="5535d-104">Selección de API</span><span class="sxs-lookup"><span data-stu-id="5535d-104">API Selection</span></span>

<span data-ttu-id="5535d-105">Como se indicó en la sección de información general, el desarrollo implica el uso de hasta tres API:</span><span class="sxs-lookup"><span data-stu-id="5535d-105">As noted in the overview section, development involves use of up to three APIs:</span></span>

-   <span data-ttu-id="5535d-106">Acceso de configuración básica: la API COM de cumplimiento mínimo de control parental (API de cumplimiento) definida en Wpcapi. h para el acceso sencillo a un subconjunto clave de estado de controles parentales.</span><span class="sxs-lookup"><span data-stu-id="5535d-106">Basic settings access: the Parental Controls minimum compliance COM API (Compliance API) defined in Wpcapi.h for simple access to a key subset of Parental Controls state.</span></span>
-   <span data-ttu-id="5535d-107">Acceso completo de lectura y escritura: el uso de un pequeño subconjunto de la API COM de WMI para el acceso completo solo es necesario si el ISV necesita modificar la configuración.</span><span class="sxs-lookup"><span data-stu-id="5535d-107">Full settings write/read access: use of a small subset of the WMI COM API for full access is only required if the ISV needs to modify settings.</span></span> <span data-ttu-id="5535d-108">La adición de un vínculo de extensibilidad de la interfaz de usuario, el reemplazo del filtro de contenido web o las adiciones a las listas de exención de filtrado de URL o aplicación HTTP para todo el equipo son los motivos principalmente para usar la API.</span><span class="sxs-lookup"><span data-stu-id="5535d-108">Addition of a UI extensibility link, replacement of the Web Content Filter, or additions to the computer-wide HTTP application or URL filtering exemption lists are the primarily reasons to use the API.</span></span> <span data-ttu-id="5535d-109">Como el uso del espacio de nombres de controles parentales de WMI proporciona acceso sin formato al almacén de configuración subyacente, los ISV deben proseguir con precaución al interpretar el estado de los valores de configuración individuales que, de hecho, pueden tener dependencias en otras opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="5535d-109">As the WMI Parental Controls namespace usage provides raw access to the underlying settings store, ISVs should proceed with caution in interpreting state from individual settings that may in fact have gating dependencies on other settings.</span></span> <span data-ttu-id="5535d-110">Por lo tanto, se recomienda usar la API de cumplimiento para leer el estado de todos los valores expuestos por esa API.</span><span class="sxs-lookup"><span data-stu-id="5535d-110">It is therefore recommended to use the Compliance API for reading state for all values exposed by that API.</span></span>
-   <span data-ttu-id="5535d-111">Registro: la API del sistema de informes y seguimiento de eventos de Windows Vista (también denominada ETW) para publicar eventos de actividad en los registros de control parental, junto con los descriptores de eventos y las enumeraciones de matriz definidos en WpcEvent. h.</span><span class="sxs-lookup"><span data-stu-id="5535d-111">Logging: the Windows Vista Event Tracing and Reporting system API (also referred to as ETW) for publishing activity events into the Parental Controls logs, in conjunction with event descriptors and array enumerations defined in WpcEvent.h.</span></span>

<span data-ttu-id="5535d-112">Todas las API se pueden llamar como un usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="5535d-112">All of the APIs are callable as a standard user.</span></span> <span data-ttu-id="5535d-113">Para el registro, cualquier usuario puede registrar eventos de registro.</span><span class="sxs-lookup"><span data-stu-id="5535d-113">For logging, any user may source log events.</span></span> <span data-ttu-id="5535d-114">Si se llama a para recuperar o cambiar la configuración de otro usuario, se producirá un error si el autor de la llamada no tiene privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="5535d-114">Calling to retrieve or change settings for another user will fail if the caller does not have administrator privileges.</span></span> <span data-ttu-id="5535d-115">En otras palabras, un usuario estándar solo puede tener acceso a su propia configuración y solo para lectura.</span><span class="sxs-lookup"><span data-stu-id="5535d-115">In other words, a standard user can access his or her own settings only, and only for reading.</span></span>

<span data-ttu-id="5535d-116">La configuración y el uso de la API de registro se describen con más detalle en estas secciones:</span><span class="sxs-lookup"><span data-stu-id="5535d-116">Settings and logging API usage are discussed further in these sections:</span></span>

-   [<span data-ttu-id="5535d-117">Uso de las API de configuración de controles parentales</span><span class="sxs-lookup"><span data-stu-id="5535d-117">Using Parental Controls Settings APIs</span></span>](using-parental-controls-settings-apis.md)
-   [<span data-ttu-id="5535d-118">Uso de las API de registro para controles parentales</span><span class="sxs-lookup"><span data-stu-id="5535d-118">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a><span data-ttu-id="5535d-119">Entorno de desarrollo</span><span class="sxs-lookup"><span data-stu-id="5535d-119">Development Environment</span></span>

<span data-ttu-id="5535d-120">El desarrollo de controles parentales requiere acceso a tres archivos de encabezado: WPC. h, WpcApi. h y WpcEvent. h.</span><span class="sxs-lookup"><span data-stu-id="5535d-120">Developing for Parental Controls requires access to three header files: Wpc.h, WpcApi.h, and WpcEvent.h.</span></span> <span data-ttu-id="5535d-121">WPC. h es un recopilador que incluye la configuración Public Compliance API y los encabezados de evento, por lo que es suficiente incluir WPC. h en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5535d-121">Wpc.h is a collector that includes the settings public compliance API and event headers, so it is sufficient to include Wpc.h in application code.</span></span>

<span data-ttu-id="5535d-122">El archivo Wpcsprov. mof especifica los permisos de lectura y escritura para la API de WMI.</span><span class="sxs-lookup"><span data-stu-id="5535d-122">Read/write permissions to the WMI API is specified by the Wpcsprov.mof file.</span></span> <span data-ttu-id="5535d-123">Este archivo se instala en el subdirectorio WBEM en el directorio system32 de Windows.</span><span class="sxs-lookup"><span data-stu-id="5535d-123">This file is installed to the WBEM subdirectory under the Windows System32 directory.</span></span>

<span data-ttu-id="5535d-124">El kit de desarrollo de software (SDK) de Microsoft Windows contiene código de ejemplo para reforzar el código de ejemplo que se muestra aquí y proporcionar herramientas orientadas a la línea de comandos simples para la exploración de API o las pruebas de integración.</span><span class="sxs-lookup"><span data-stu-id="5535d-124">The Microsoft Windows Software Development Kit (SDK) contains sample code to reinforce example code shown here and provide simple command-line driven tools for API exploration or integration testing.</span></span>

 

 



