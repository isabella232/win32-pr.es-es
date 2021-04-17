---
description: La tabla DisplayToID relaciona la cadena descriptiva que muestra el monitor de sistema con el GUID almacenado en las otras tablas.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667332"
---
# <a name="displaytoid"></a><span data-ttu-id="b6aa7-103">DisplayToID</span><span class="sxs-lookup"><span data-stu-id="b6aa7-103">DisplayToID</span></span>

<span data-ttu-id="b6aa7-104">La tabla **DisplayToID** relaciona la cadena descriptiva que muestra el monitor de sistema con el GUID almacenado en las otras tablas.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-104">The **DisplayToID** table relates the user-friendly string displayed by the System Monitor to the GUID stored in the other tables.</span></span>

<span data-ttu-id="b6aa7-105">La tabla **DisplayToID** define los campos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6aa7-105">The **DisplayToID** table defines the following fields:</span></span>

-   <span data-ttu-id="b6aa7-106">**GUID:** Identificador único generado para un registro.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-106">**GUID:** Unique identifier generated for a log.</span></span> <span data-ttu-id="b6aa7-107">Este campo es la clave principal de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="b6aa7-108">**RunID:** Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-108">**RunID:** Reserved for internal use.</span></span>
-   <span data-ttu-id="b6aa7-109">**DisplayString:** Nombre del archivo de registro que se muestra en el monitor de sistema.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-109">**DisplayString:** Name of the log file as displayed in the System Monitor.</span></span>
-   <span data-ttu-id="b6aa7-110">**LogStartTime:** Hora en que se inició el proceso de registro en formato AAAA-MM-DD HH: mm: SS: nnn.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-110">**LogStartTime:** Time the logging process started in yyyy-mm-dd hh:mm:ss:nnn format.</span></span>
-   <span data-ttu-id="b6aa7-111">**LogStopTime:** Hora en que el proceso de registro se detuvo en el formato AAAA-MM-DD HH: mm: SS: nnn.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-111">**LogStopTime:** Time the logging process stopped in yyyy-mm-dd hh:mm:ss:nnn format.</span></span> <span data-ttu-id="b6aa7-112">Se pueden diferenciar varios archivos de registro con el mismo valor **DisplayString** usando el valor de los campos y **LogStartTime** .</span><span class="sxs-lookup"><span data-stu-id="b6aa7-112">Multiple log files with the same **DisplayString** value can be differentiated by using the value in this and the **LogStartTime** fields.</span></span> <span data-ttu-id="b6aa7-113">Los valores de los campos **LogStartTime** y **LogStopTime** también permiten acceder rápidamente al tiempo total de recopilación.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-113">The values in the **LogStartTime** and **LogStopTime** fields also allows the total collection time to be accessed quickly.</span></span>
-   <span data-ttu-id="b6aa7-114">**NumberOfRecords:** Número de muestras almacenadas en la tabla para cada colección de registros.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-114">**NumberOfRecords:** Number of samples stored in the table for each log collection.</span></span>
-   <span data-ttu-id="b6aa7-115">**MinutesToUTC:** Valor que se usa para convertir los datos de fila almacenados en hora UTC en hora local.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-115">**MinutesToUTC:** Value used to convert the row data stored in UTC time to local time.</span></span>
-   <span data-ttu-id="b6aa7-116">**TimeZoneName:** Nombre de la zona horaria en la que se recopilaron los datos.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-116">**TimeZoneName:** Name of the time zone where the data was collected.</span></span> <span data-ttu-id="b6aa7-117">Si va a recopilar datos de un archivo recopilado en sistemas que se encuentran en su propia zona horaria, este campo indicará la ubicación.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-117">If you are collecting or have relogged data from a file collected on systems in your own time zone, this field will state the location.</span></span>

<span data-ttu-id="b6aa7-118">**Nota:**  Antes de Windows Vista, los conjuntos de recopiladores de datos se almacenaban en el registro en</span><span class="sxs-lookup"><span data-stu-id="b6aa7-118">**Note**  Prior to Windows Vista, the data collector sets were stored in the registry at</span></span>

<span data-ttu-id="b6aa7-119">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ SysmonLog \\ log queries**</span><span class="sxs-lookup"><span data-stu-id="b6aa7-119">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\SysmonLog\\Log Queries**</span></span>

<span data-ttu-id="b6aa7-120">.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-120">.</span></span> <span data-ttu-id="b6aa7-121">Los campos enumerados anteriormente no corresponden a los valores del registro.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-121">The fields listed above do not correspond to the values in registry.</span></span> <span data-ttu-id="b6aa7-122">En Windows Vista, los conjuntos de recopiladores de datos no se almacenan en el registro.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-122">For Windows Vista, the data collector sets are not stored in the registry.</span></span>

 

 



