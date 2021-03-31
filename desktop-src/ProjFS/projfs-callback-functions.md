---
title: Funciones de devolución de llamada ProjFS
description: Las siguientes funciones de devolución de llamada se declaran en projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "103904371"
---
# <a name="callback-functions"></a><span data-ttu-id="8a385-103">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="8a385-103">Callback functions</span></span>

<span data-ttu-id="8a385-104">Las siguientes funciones de devolución de llamada se declaran en projectedfslib. h.</span><span class="sxs-lookup"><span data-stu-id="8a385-104">The following callback functions are declared in projectedfslib.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8a385-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8a385-105">In this section</span></span>

| <span data-ttu-id="8a385-106">Tema</span><span class="sxs-lookup"><span data-stu-id="8a385-106">Topic</span></span> | <span data-ttu-id="8a385-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a385-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="8a385-108">**PRJ_CANCEL_COMMAND_CB**</span><span class="sxs-lookup"><span data-stu-id="8a385-108">**PRJ_CANCEL_COMMAND_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | <span data-ttu-id="8a385-109">Notifica al proveedor que se debe cancelar una operación mediante una invocación anterior de una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a385-109">Notifies the provider that an operation by an earlier invocation of a callback should be canceled.</span></span> |
| [<span data-ttu-id="8a385-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="8a385-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | <span data-ttu-id="8a385-111">Informa al proveedor de que la enumeración de un directorio ha superado.</span><span class="sxs-lookup"><span data-stu-id="8a385-111">Informs the provider that a directory enumeration is over.</span></span> |
| [<span data-ttu-id="8a385-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="8a385-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | <span data-ttu-id="8a385-113">Solicita información de enumeración de directorio del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8a385-113">Requests directory enumeration information from the provider.</span></span>
| [<span data-ttu-id="8a385-114">**PRJ_GET_FILE_DATA_CB**</span><span class="sxs-lookup"><span data-stu-id="8a385-114">**PRJ_GET_FILE_DATA_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | <span data-ttu-id="8a385-115">Solicita el contenido del flujo de datos principal de un archivo.</span><span class="sxs-lookup"><span data-stu-id="8a385-115">Requests the contents of a file's primary data stream.</span></span>
| [<span data-ttu-id="8a385-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span><span class="sxs-lookup"><span data-stu-id="8a385-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | <span data-ttu-id="8a385-117">Solicita información para un archivo o directorio del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8a385-117">Requests information for a file or directory from the provider.</span></span>
| [<span data-ttu-id="8a385-118">**PRJ_NOTIFICATION_CB**</span><span class="sxs-lookup"><span data-stu-id="8a385-118">**PRJ_NOTIFICATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | <span data-ttu-id="8a385-119">Entrega las notificaciones al proveedor acerca de las operaciones del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="8a385-119">Delivers notifications to the provider about file system operations.</span></span>
| [<span data-ttu-id="8a385-120">**PRJ_QUERY_FILE_NAME_CB**</span><span class="sxs-lookup"><span data-stu-id="8a385-120">**PRJ_QUERY_FILE_NAME_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | <span data-ttu-id="8a385-121">Determina si una ruta de acceso de archivo determinada existe en la memoria auxiliar del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8a385-121">Determines whether a given file path exists in the provider's backing store.</span></span>
| [<span data-ttu-id="8a385-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="8a385-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | <span data-ttu-id="8a385-123">Informa al proveedor de que se está iniciando una enumeración de directorios.</span><span class="sxs-lookup"><span data-stu-id="8a385-123">Informs the provider that a directory enumeration is starting.</span></span>