---
title: SYSMON valores devueltos
description: A continuación se muestra una lista de los valores devueltos del monitor de sistema que se definen en Smonmsg. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421129"
---
# <a name="sysmon-return-values"></a><span data-ttu-id="a087c-103">SYSMON valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a087c-103">SYSMON Return Values</span></span>

<span data-ttu-id="a087c-104">A continuación se muestra una lista de los valores devueltos del monitor de sistema que se definen en Smonmsg. h.</span><span class="sxs-lookup"><span data-stu-id="a087c-104">The following is a list of the System Monitor return values that are defined in Smonmsg.h.</span></span>



| <span data-ttu-id="a087c-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a087c-105">Return value</span></span>                                       | <span data-ttu-id="a087c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a087c-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a087c-107">SMON \_ estado \_ DUPL \_ ruta de acceso de contador \_ (0xC0001388)</span><span class="sxs-lookup"><span data-stu-id="a087c-107">SMON\_STATUS\_DUPL\_COUNTER\_PATH (0xC0001388)</span></span>     | <span data-ttu-id="a087c-108">La colección de contadores ya contiene el contador especificado.</span><span class="sxs-lookup"><span data-stu-id="a087c-108">The counter collection already contains the specified counter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="a087c-109">Estado de SMON \_ \_ no \_ \_ objeto SYSMON (0xC0001389)</span><span class="sxs-lookup"><span data-stu-id="a087c-109">SMON\_STATUS\_NO\_SYSMON\_OBJECT (0xC0001389)</span></span>      | <span data-ttu-id="a087c-110">La configuración no contiene ningún objeto HTML de monitor de sistema completo.</span><span class="sxs-lookup"><span data-stu-id="a087c-110">The settings do not contain any complete System Monitor HTML objects.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="a087c-111">SMON \_ status \_ Too \_ pocas \_ Samples (0xC000138A)</span><span class="sxs-lookup"><span data-stu-id="a087c-111">SMON\_STATUS\_TOO\_FEW\_SAMPLES (0xC000138A)</span></span>       | <span data-ttu-id="a087c-112">El archivo de registro especificado contiene menos de dos muestras de datos.</span><span class="sxs-lookup"><span data-stu-id="a087c-112">The specified log file contains fewer than two data samples.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="a087c-113">\_Límite de \_ tamaño del archivo de registro de estado de SMON \_ \_ \_ (0xC000138B)</span><span class="sxs-lookup"><span data-stu-id="a087c-113">SMON\_STATUS\_LOG\_FILE\_SIZE\_LIMIT (0xC000138B)</span></span>  | <span data-ttu-id="a087c-114">El archivo de registro especificado supera los límites de tamaño del control de monitor del sistema.</span><span class="sxs-lookup"><span data-stu-id="a087c-114">The specified log file exceeds the size limits of the System Monitor control.</span></span> <span data-ttu-id="a087c-115">Si hay un archivo de registro seleccionado, seleccione actividad actual como origen de datos para descargar el archivo de registro actual y, a continuación, vuelva a seleccionar el archivo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="a087c-115">If a log file is currently selected, select current activity as the data source in order to unload the current log file, then reselect the specified log file.</span></span> |
| <span data-ttu-id="a087c-116">\_Origen de \_ datos del archivo de registro de estado de SMON \_ \_ \_ (0xC000138C)</span><span class="sxs-lookup"><span data-stu-id="a087c-116">SMON\_STATUS\_LOG\_FILE\_DATA\_SOURCE (0xC000138C)</span></span> | <span data-ttu-id="a087c-117">Para agregar un nuevo archivo de registro al origen de datos, el tipo de origen de datos debe cambiarse a un tipo distinto de sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="a087c-117">To add a new log file to the data source, the data source type must be changed to a type other than sysmonLogFiles.</span></span>                                                                                                                          |
| <span data-ttu-id="a087c-118">SMON \_ status \_ DUPL \_ \_ ruta de acceso del archivo de registro \_ (0xC000138D)</span><span class="sxs-lookup"><span data-stu-id="a087c-118">SMON\_STATUS\_DUPL\_LOG\_FILE\_PATH (0xC000138D)</span></span>   | <span data-ttu-id="a087c-119">La colección de archivos de registro ya contiene el archivo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="a087c-119">The log file collection already contains the specified log file.</span></span>                                                                                                                                                                             |



 

<span data-ttu-id="a087c-120">Para obtener una descripción de los valores devueltos adicionales devueltos por el monitor de sistema, vea códigos de [error del sistema](/windows/desktop/Debug/system-error-codes) y códigos de error de la [aplicación auxiliar de datos de rendimiento](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span><span class="sxs-lookup"><span data-stu-id="a087c-120">For a description of additional return values returned by System Monitor, see [System Error Codes](/windows/desktop/Debug/system-error-codes) and [Performance Data Helper Error Codes](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span></span>

 

 