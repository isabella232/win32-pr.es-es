---
description: Configuración del registro de errores
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Configuración del registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677028"
---
# <a name="setting-the-error-log"></a><span data-ttu-id="79d38-103">Configuración del registro de errores</span><span class="sxs-lookup"><span data-stu-id="79d38-103">Setting the Error Log</span></span>

<span data-ttu-id="79d38-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="79d38-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="79d38-105">Después de implementar la clase de registro de errores, cree una nueva instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="79d38-105">After you implement the error logging class, create a new instance of the class.</span></span> <span data-ttu-id="79d38-106">A continuación, proporcione a los [servicios de edición de DirectShow](directshow-editing-services.md) un puntero a él llamando al método de [**\_ ErrorLog IAMSetErrorLog::p UT**](iamseterrorlog-put-errorlog.md) en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="79d38-106">Then, give [DirectShow Editing Services](directshow-editing-services.md) a pointer to it by calling the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span> <span data-ttu-id="79d38-107">Consulte la escala de tiempo de la interfaz **IAMSetErrorLog** .</span><span class="sxs-lookup"><span data-stu-id="79d38-107">Query the timeline for the **IAMSetErrorLog** interface.</span></span> <span data-ttu-id="79d38-108">Para asegurarse de que se registran todos los errores, debe llamar a este método antes de cargar, guardar o representar la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="79d38-108">To ensure that all errors are logged, you should call this method before you load, save, or render the timeline.</span></span>


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



<span data-ttu-id="79d38-109">El registro de errores no tiene ningún efecto en los valores devueltos que recibe cuando se llama a métodos en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79d38-109">Error logging has no effect on the return values that you receive when you call methods in your application.</span></span> <span data-ttu-id="79d38-110">El registro de errores complementa, pero no reemplaza las técnicas habituales de control de errores.</span><span class="sxs-lookup"><span data-stu-id="79d38-110">Error logging complements but does not replace the usual error handling techniques.</span></span> <span data-ttu-id="79d38-111">Para crear una aplicación sólida, compruebe siempre los valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="79d38-111">To create a robust application, always check HRESULT values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79d38-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79d38-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79d38-113">Errores de registro</span><span class="sxs-lookup"><span data-stu-id="79d38-113">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



