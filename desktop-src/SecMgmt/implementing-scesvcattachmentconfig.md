---
description: Debe recuperar información de la base de datos de seguridad y, a continuación, utilizar esa información para configurar el servicio.
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: Implementación de SceSvcAttachmentConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98eb519e6422e3036ddfb203811322befd2713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002469"
---
# <a name="implementing-scesvcattachmentconfig"></a><span data-ttu-id="ef973-103">Implementación de SceSvcAttachmentConfig</span><span class="sxs-lookup"><span data-stu-id="ef973-103">Implementing SceSvcAttachmentConfig</span></span>

<span data-ttu-id="ef973-104">La función [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) debe recuperar información de la base de datos de seguridad y, a continuación, utilizar esa información para configurar el servicio.</span><span class="sxs-lookup"><span data-stu-id="ef973-104">The [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) function must retrieve information from the security database and then use that information to configure the service.</span></span>

<span data-ttu-id="ef973-105">Al implementar [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), puede recuperar toda la información y, a continuación, configurar el servicio, o bien recuperar y configurar el servicio en pasos.</span><span class="sxs-lookup"><span data-stu-id="ef973-105">When implementing [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), you can either retrieve all of the information and then configure the service, or retrieve and configure the service in steps.</span></span> <span data-ttu-id="ef973-106">El siguiente algoritmo recupera toda la información y, a continuación, configura el servicio.</span><span class="sxs-lookup"><span data-stu-id="ef973-106">The following algorithm retrieves all of the information and then configures the service.</span></span>

<span data-ttu-id="ef973-107">**Para implementar SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="ef973-107">**To implement SceSvcAttachmentConfig**</span></span>

1.  <span data-ttu-id="ef973-108">Defina las variables necesarias para recuperar información y códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="ef973-108">Define the variables needed to retrieve information and return codes.</span></span>
2.  <span data-ttu-id="ef973-109">Llame a la función de devolución de llamada pfQueryInfo en la estructura de devolución de llamada para recuperar información de configuración de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ef973-109">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="ef973-110">Configure el sistema con la información devuelta.</span><span class="sxs-lookup"><span data-stu-id="ef973-110">Configure the system with the returned information.</span></span>
4.  <span data-ttu-id="ef973-111">Llame a la función de devolución de llamada pfFreeInfo en la estructura de devolución de llamada para liberar la memoria usada para la información devuelta.</span><span class="sxs-lookup"><span data-stu-id="ef973-111">Call the pfFreeInfo callback function in the callback structure to free memory used for returned information.</span></span>
5.  <span data-ttu-id="ef973-112">Si hay algún mensaje que la extensión desee agregar al archivo de registro de análisis, llame a la función de devolución de llamada pfLogInfo en la estructura de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ef973-112">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
6.  <span data-ttu-id="ef973-113">Devuelve los códigos de **SCESTATUS** apropiados.</span><span class="sxs-lookup"><span data-stu-id="ef973-113">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="ef973-114">En el ejemplo siguiente se muestra una posible implementación de [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="ef973-114">The following example shows one possible implementation of [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span></span> <span data-ttu-id="ef973-115">Tenga en cuenta que en este ejemplo, la función ProcessConfigurationLine establece la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="ef973-115">Note that in this example, the function ProcessConfigurationLine sets the service configuration.</span></span> <span data-ttu-id="ef973-116">No se muestra la implementación de esta función.</span><span class="sxs-lookup"><span data-stu-id="ef973-116">The implementation of this function is not shown.</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo
)
{
  
  ////////////////////////////////////////////////////
  // Define variables.
  ////////////////////////////////////////////////////
     PSCESVC_CONFIGURATION_INFO     pConfigInfo = NULL;
     SCESTATUS                      retCode;
     SCE_ENUMERATION_CONTEXT        EnumContext = 0;
  
     if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ) 
     {
        return(SCESTATUS_INVALID_PARAMETER);
     }
  
  
      ////////////////////////////////////////////////////
      // Retrieve configuration information and configure
      // system. 
      ////////////////////////////////////////////////////
      do
      {
            retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                  SceSvcConfigurationInfo,
                                  NULL,
                                  FALSE,
                                  (PVOID *)&pConfigInfo,
                                  &EnumContext
                                 );
            if (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
            {
              ULONG i:
              //////////////////////////////////////////////////
              // Configure system.
              /////////////////////////////////////////////////
              for(i = 0; < pConfigInfo->Count; i++)
              {
                if(pConfigInfo->Line[i].Key == NULL) 
                    continue;
                ProcessConfigurationLine(pConfigInfo->Line[i]);
              }
      
      
              //////////////////////////////////////////////////
              // Free data returned.
              /////////////////////////////////////////////////
              (*(pSceCbInfo->pfFreeInfo)) ((PVOPID)pConfigInfo);
              pConfigInfo = NULL;
            }
        } while (retCode == SCESTATUS_SUCCESS && CountReturned > 0);
  
  
  ////////////////////////////////////////////////////
  // Add code for other return codes if retCode is 
  // not SCESTATUS_SUCCESS.
  ///////////////////////////////////////////////////
  return retCode;
}
```



 

 



