---
description: La herramienta Unlodctr quita las entradas del registro creadas por LODCTR.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Quitar nombres y descripciones de contadores del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667252"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a><span data-ttu-id="a9ee7-103">Quitar nombres y descripciones de contadores del registro</span><span class="sxs-lookup"><span data-stu-id="a9ee7-103">Removing Counter Names and Descriptions from the Registry</span></span>

<span data-ttu-id="a9ee7-104">La herramienta **Unlodctr** quita las entradas del registro creadas por **LODCTR**.</span><span class="sxs-lookup"><span data-stu-id="a9ee7-104">The **unlodctr** tool removes the registry entries created by **lodctr**.</span></span> <span data-ttu-id="a9ee7-105">El nombre de la aplicación que pase a **Unlodctr** debe coincidir con el [nombre de la clave de aplicación](creating-the-applications-performance-key.md) que creó en la clave **servicios** .</span><span class="sxs-lookup"><span data-stu-id="a9ee7-105">The application name that you pass to **unlodctr** must match the [name of the application key](creating-the-applications-performance-key.md) that you created under the **Services** key.</span></span> <span data-ttu-id="a9ee7-106">Para obtener más información sobre cómo ejecutar **Unlodctr** , vea el centro de ayuda y soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="a9ee7-106">For details on running **unlodctr** see, Help and Support Center.</span></span>

## <a name="using-unlodctr"></a><span data-ttu-id="a9ee7-107">Usar Unlodctr</span><span class="sxs-lookup"><span data-stu-id="a9ee7-107">Using unlodctr</span></span>

<span data-ttu-id="a9ee7-108">La herramienta **Unlodctr** busca el primer y último contador y los valores de índice de la ayuda usando los valores del registro con el mismo nombre en la clave de **rendimiento** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a9ee7-108">The **unlodctr** tool looks up the first and last counter and help index values using the like named registry values under your application's **Performance** key.</span></span> <span data-ttu-id="a9ee7-109">La herramienta **Unlodctr** usa el intervalo de valores de índice para quitar el texto de los **contadores** y los valores de **ayuda** de cada identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="a9ee7-109">The **unlodctr** tool uses the range of index values to remove the text from **Counters** and **Help** values for each language identifier.</span></span>

<span data-ttu-id="a9ee7-110">Con los valores de índice, **Unlodctr** realiza los siguientes cambios en el registro.</span><span class="sxs-lookup"><span data-stu-id="a9ee7-110">Using the index values, **unlodctr** makes the following changes to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

<span data-ttu-id="a9ee7-111">La herramienta **Unlodctr** también quita los valores del **primer contador**, **último contador**, **primera ayuda**, **última ayuda** y **lista de objetos** de la clave de **rendimiento** de la aplicación que se encuentra en **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *Application-Name* \\ **performance**.</span><span class="sxs-lookup"><span data-stu-id="a9ee7-111">The **unlodctr** tool also removes the **First Counter**, **Last Counter**, **First Help**, **Last Help**, and **Object List** values from the application's **Performance** key located at **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\*application-name*\\**Performance**.</span></span>

> [!Note]  
> <span data-ttu-id="a9ee7-112">La función de descarga de **Unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), se declara en Loadperf. h y se exporta desde Loadperf.dll.</span><span class="sxs-lookup"><span data-stu-id="a9ee7-112">The unloading function of **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), is declared in Loadperf.h and exported from Loadperf.dll.</span></span> <span data-ttu-id="a9ee7-113">Esto le permite llamar a esta función directamente desde el programa de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="a9ee7-113">This allows you to call this function directly from your uninstall program.</span></span>

 

 

 



