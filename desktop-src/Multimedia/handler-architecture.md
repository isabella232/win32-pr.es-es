---
title: Arquitectura de controlador
description: Arquitectura de controlador
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075824"
---
# <a name="handler-architecture"></a><span data-ttu-id="88a27-103">Arquitectura de controlador</span><span class="sxs-lookup"><span data-stu-id="88a27-103">Handler Architecture</span></span>

<span data-ttu-id="88a27-104">La función interna de un controlador de archivo o secuencia se define mediante el propio controlador.</span><span class="sxs-lookup"><span data-stu-id="88a27-104">The internal function of a file or stream handler is defined by the handler itself.</span></span> <span data-ttu-id="88a27-105">Para una aplicación, un controlador de archivos aparece normalmente como un módulo para leer y escribir archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="88a27-105">To an application, a file handler typically appears as a module to read and write AVI files.</span></span> <span data-ttu-id="88a27-106">Del mismo modo, un controlador de flujo aparece como un módulo para leer y escribir un tipo específico de flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="88a27-106">Similarly, a stream handler appears as a module to read and write a specific type of data stream.</span></span> <span data-ttu-id="88a27-107">La interfaz de flujo coherente hace que el origen y el destino de la secuencia no sean importantes para la aplicación que utiliza el controlador.</span><span class="sxs-lookup"><span data-stu-id="88a27-107">The consistent stream interface makes the source and destination of the stream unimportant to the application that uses the handler.</span></span>

<span data-ttu-id="88a27-108">Un controlador de archivos proporciona acceso a un origen de datos que consta de uno o varios flujos de datos.</span><span class="sxs-lookup"><span data-stu-id="88a27-108">A file handler provides access to a data source consisting of one or more data streams.</span></span> <span data-ttu-id="88a27-109">Los controladores de archivos proporcionan normalmente acceso a archivos de disco que contienen uno o más flujos de datos, y las funciones internas del controlador de archivos leen y escriben los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="88a27-109">File handlers typically provide access to disk files containing one or more data streams, and the internal functions of the file handler read and write the multimedia data.</span></span> <span data-ttu-id="88a27-110">Sin embargo, los controladores de archivo pueden trabajar con cualquier origen de datos, como un canal de transmisión digital que contiene varios flujos de datos mezclados.</span><span class="sxs-lookup"><span data-stu-id="88a27-110">However, file handlers can work with any data source, such as a digital transmission channel containing several intermingled data streams.</span></span>

<span data-ttu-id="88a27-111">En cambio, un controlador de flujo procesa un tipo de datos y aparece como un flujo de datos en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="88a27-111">In contrast, a stream handler processes one type of data and appears as a data stream to an application.</span></span> <span data-ttu-id="88a27-112">Un controlador de flujo puede proporcionar datos que fabrica o puede recuperar datos de un archivo o de un origen externo.</span><span class="sxs-lookup"><span data-stu-id="88a27-112">A stream handler can provide data that it manufactures, or it can retrieve data from a file or an external source.</span></span> <span data-ttu-id="88a27-113">Proporciona sus datos en un formato que pueda usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88a27-113">It supplies its data in a format that your application can use.</span></span>

 

 




