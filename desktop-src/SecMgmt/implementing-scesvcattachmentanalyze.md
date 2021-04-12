---
description: Debe recuperar la información de configuración de la base de datos de seguridad y del servicio, comparar los dos conjuntos de información y, a continuación, actualizar la sección de análisis de la base de datos de seguridad con cualquier diferencia.
ms.assetid: f8420dde-55a2-40a0-b10d-140c28c0e9e4
title: Implementación de SceSvcAttachmentAnalyze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f8501be2caac84c3dc96363eb85a8bc787d2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277955"
---
# <a name="implementing-scesvcattachmentanalyze"></a><span data-ttu-id="3c57c-103">Implementación de SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="3c57c-103">Implementing SceSvcAttachmentAnalyze</span></span>

<span data-ttu-id="3c57c-104">La función [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) debe recuperar la información de configuración de la base de datos de seguridad y el servicio, comparar los dos conjuntos de información y, a continuación, actualizar la sección de análisis de la base de datos de seguridad con cualquier diferencia.</span><span class="sxs-lookup"><span data-stu-id="3c57c-104">The [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) function must retrieve configuration information from the security database and the service, compare the two sets of information, and then update the analysis section of the security database with any differences.</span></span> <span data-ttu-id="3c57c-105">Puede asegurarse de esto mediante el siguiente algoritmo.</span><span class="sxs-lookup"><span data-stu-id="3c57c-105">You can ensure this by using the following algorithm.</span></span>

<span data-ttu-id="3c57c-106">**Para implementar SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="3c57c-106">**To implement SceSvcAttachmentAnalyze**</span></span>

1.  <span data-ttu-id="3c57c-107">Defina las variables necesarias para recuperar y establecer la información de seguridad y los códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="3c57c-107">Define the variables needed to retrieve and set the security information and return codes.</span></span>
2.  <span data-ttu-id="3c57c-108">Llame a la función de devolución de llamada pfQueryInfo en la estructura de devolución de llamada para recuperar información de configuración de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3c57c-108">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="3c57c-109">Recupere la información correspondiente del servicio.</span><span class="sxs-lookup"><span data-stu-id="3c57c-109">Retrieve the corresponding information from the service.</span></span>
4.  <span data-ttu-id="3c57c-110">Compare los datos de configuración recuperados del servicio con que se recuperaron de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3c57c-110">Compare the configuration data retrieved from the service with that retrieved from the security database.</span></span>
5.  <span data-ttu-id="3c57c-111">Si la información no es igual, llame a la función de devolución de llamada pfSetInfo en la estructura de devolución de llamada para actualizar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3c57c-111">If the information is not the same, call the pfSetInfo callback function in the callback structure to update the database.</span></span>
6.  <span data-ttu-id="3c57c-112">Libere todos los búferes utilizados para recuperar información.</span><span class="sxs-lookup"><span data-stu-id="3c57c-112">Free all buffers used to retrieve information.</span></span> <span data-ttu-id="3c57c-113">Llame a la función de devolución de llamada pfFreeInfo en la estructura de devolución de llamada para liberar la memoria usada para la información de base de datos devuelta.</span><span class="sxs-lookup"><span data-stu-id="3c57c-113">Call the pfFreeInfo callback function in the callback structure to free memory used for returned database information.</span></span>
7.  <span data-ttu-id="3c57c-114">Si hay algún mensaje que la extensión desee agregar al archivo de registro de análisis, llame a la función de devolución de llamada pfLogInfo en la estructura de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3c57c-114">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
8.  <span data-ttu-id="3c57c-115">Devuelve los códigos de **SCESTATUS** apropiados.</span><span class="sxs-lookup"><span data-stu-id="3c57c-115">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="3c57c-116">En el ejemplo siguiente se muestra una posible implementación de [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="3c57c-116">The following example shows one possible implementation of [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span></span> <span data-ttu-id="3c57c-117">Tenga en cuenta que en este ejemplo, las funciones QueryConfigurationLine y CompareValue consultan respectivamente la información del servicio y comparan esos valores con los recuperados de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3c57c-117">Note that in this example, the functions QueryConfigurationLine and CompareValue respectively query information from the service and compare those values with those retrieved from the security database.</span></span> <span data-ttu-id="3c57c-118">No se muestra la implementación de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="3c57c-118">The implementation of these functions is not shown.</span></span>


```C++
#include <windows.h>

SCESTATUS WINAPI SceSvcAttachmentAnalyze (
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
  // Retrieve information from security database.
  ///////////////////////////////////////////////////
    do
    {
        retCode =  (*(pSceCbInfo->pfQueryInfo))(
                              pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              NULL,
                              FALSE,
                              &pConfigInfo,
                              &EnumContext
                              );
        if(retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
        {
          ULONG i;
          for(i = 0;i < pConfigInfo->Count; i++)
          {
            if(pConfigInfo->Line[I].Key == NULL) 
                continue;
        
        //////////////////////////////////////////////
        // Query service for corresponding key.
        //////////////////////////////////////////////
            QueryConfigurationLine(
                               pConfigInfo->Line[i].Key,
                               &SystemValue);
        
        //////////////////////////////////////////////
        // Compare values.
        //////////////////////////////////////////////
            CompareValue(
                     pConfigInfo->Line[i].Key,
                     SystemValue,
                     pConfigInfo->Line[i].Value,
                     &Result);
        
        //////////////////////////////////////////////
        // Write to security database if values are 
        // not equal.
        //////////////////////////////////////////////
            if(Result != NULL)
            {
              retCode =  (*(pSceCbInfo->pfSetInfo))(pSceCbInfo->sceHandle,
                                      SceSvcAnalysisInfo,
                                      pConfigInfo->Line[i].Key,
                                      TRUE,
                                      Result);
              if(retCode != SCESTATUS_SUCCESS)
              {
                //////////////////////////////////////////
                // Add code to handle other return codes.
                //////////////////////////////////////////
              }
            }
        }
      
          //////////////////////////////////////////////
          // Free all buffers used to retrieve 
          // SceSvcFree frees memory allocated by call 
          // to SceSvcQueryQueryInfo. 
          /////////////////////////////////////////
        (*(pSceCbInfo->pfFreeInfo)) (PVOID)pConfigInfo);
          pConfigInfo = NULL;
    }
  } while (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL);
  
  
  //////////////////////////////////////////////////
  // If the return code is not SCESTATUS_SUCCESS, add code to 
  // set error message appropriately.
  //////////////////////////////////////////////////
  return retCode;
}
```



 

 



