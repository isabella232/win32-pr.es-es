---
description: El objeto de informe de datos de sensor contiene datos de sensor.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Objeto de informe de datos de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d43753aa28be5cd20c85b7e65bf4c7516d4c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002333"
---
# <a name="the-sensor-data-report-object"></a><span data-ttu-id="e21a7-103">Objeto de informe de datos de sensor</span><span class="sxs-lookup"><span data-stu-id="e21a7-103">The Sensor Data Report Object</span></span>

<span data-ttu-id="e21a7-104">El objeto de informe de datos de sensor contiene datos de sensor.</span><span class="sxs-lookup"><span data-stu-id="e21a7-104">The sensor data report object contains sensor data.</span></span>

<span data-ttu-id="e21a7-105">Para que un sensor sea útil, debe proporcionar datos significativos.</span><span class="sxs-lookup"><span data-stu-id="e21a7-105">For a sensor to be useful, it must provide meaningful data.</span></span> <span data-ttu-id="e21a7-106">La cantidad y la frecuencia de generación de datos varían de un sensor a un sensor.</span><span class="sxs-lookup"><span data-stu-id="e21a7-106">The amount and frequency of data generation varies from sensor to sensor.</span></span> <span data-ttu-id="e21a7-107">Por ejemplo, un sensor que detecta si una puerta está abierta generará una pequeña cantidad de datos **booleanos** , mientras que un sensor de movimiento podría generar continuamente varios elementos de datos.</span><span class="sxs-lookup"><span data-stu-id="e21a7-107">For example, a sensor that detects whether a door is open would generate a small amount of **Boolean** data, while a motion sensor might continuously generate multiple data items.</span></span> <span data-ttu-id="e21a7-108">Para estandarizar la forma en que el programa recibe los datos, la API de sensor usa el objeto de informe de datos de sensor.</span><span class="sxs-lookup"><span data-stu-id="e21a7-108">To standardize the way your program receives data, the Sensor API uses the sensor data report object.</span></span>

<span data-ttu-id="e21a7-109">Puede tener acceso a la información de un informe de datos de sensor a través de la interfaz [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) .</span><span class="sxs-lookup"><span data-stu-id="e21a7-109">You can access the information in a sensor data report through the [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) interface.</span></span> <span data-ttu-id="e21a7-110">Esta interfaz le permite recuperar la marca de tiempo del informe de datos para que pueda determinar si la información del informe es útil.</span><span class="sxs-lookup"><span data-stu-id="e21a7-110">This interface lets you retrieve the data report's time stamp so that you can determine whether the information in the report is useful.</span></span> <span data-ttu-id="e21a7-111">Puede recuperar los datos en sí de dos maneras: como un valor de campo de datos individual o como un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="e21a7-111">You can retrieve the data itself in two ways: as an individual data field value or as a set of values.</span></span> <span data-ttu-id="e21a7-112">Para recuperar los datos como un valor individual, llame al método [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) .</span><span class="sxs-lookup"><span data-stu-id="e21a7-112">To retrieve data as an individual value, call the [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) method.</span></span> <span data-ttu-id="e21a7-113">Para recuperar varios valores, llame al método [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) .</span><span class="sxs-lookup"><span data-stu-id="e21a7-113">To retrieve multiple values, call the [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) method.</span></span>

<span data-ttu-id="e21a7-114">Especifique el tipo de datos o campos de datos que desea recuperar del informe mediante una constante **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="e21a7-114">You specify the type of data, or data fields, that you want to retrieve from the report by using a **PROPERTYKEY** constant.</span></span> <span data-ttu-id="e21a7-115">Las claves de propiedad de los campos de datos de los tipos de sensor comunes se definen en Sensors. h.</span><span class="sxs-lookup"><span data-stu-id="e21a7-115">Property keys for data fields of common sensor types are defined in Sensors.h.</span></span>

 

 
