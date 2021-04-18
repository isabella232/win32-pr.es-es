---
description: Toma como parámetro un conjunto de información de configuración proporcionada.
ms.assetid: 3c0a71f6-f643-4a5e-8b5c-15c976a3736e
title: Implementación de SceSvcAttachmentUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381a2b04b75399b5f580426d9f2dd9f5911f52d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687578"
---
# <a name="implementing-scesvcattachmentupdate"></a><span data-ttu-id="9e4de-103">Implementación de SceSvcAttachmentUpdate</span><span class="sxs-lookup"><span data-stu-id="9e4de-103">Implementing SceSvcAttachmentUpdate</span></span>

<span data-ttu-id="9e4de-104">La función [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md) toma como parámetro un conjunto de información de configuración proporcionada.</span><span class="sxs-lookup"><span data-stu-id="9e4de-104">The [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md) function takes as a parameter a set of supplied configuration information.</span></span> <span data-ttu-id="9e4de-105">A continuación, recupera la información de la base de datos de seguridad, calcula una nueva configuración base con la información de configuración proporcionada, calcula la nueva información de análisis basada en la información de la base de datos y la información de configuración proporcionada, y actualiza la base de datos con la nueva configuración base y la información de análisis.</span><span class="sxs-lookup"><span data-stu-id="9e4de-105">It then retrieves information from the security database, computes a new base configuration using the supplied configuration information, computes new analysis information based on the database information and the supplied configuration information, and updates the database with new base configuration and analysis information.</span></span> <span data-ttu-id="9e4de-106">Puede implementar **SceSvcAttachmentUpdate** mediante el siguiente algoritmo.</span><span class="sxs-lookup"><span data-stu-id="9e4de-106">You can implement **SceSvcAttachmentUpdate** by using the following algorithm.</span></span>

<span data-ttu-id="9e4de-107">**Para implementar SceSvcAttachmentUpdate**</span><span class="sxs-lookup"><span data-stu-id="9e4de-107">**To implement SceSvcAttachmentUpdate**</span></span>

1.  <span data-ttu-id="9e4de-108">Defina las variables necesarias para recuperar información, establecer información y códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="9e4de-108">Define the variables needed to retrieve information, set information, and return codes.</span></span>
2.  <span data-ttu-id="9e4de-109">Llame a la función de devolución de llamada pfQueryInfo en la estructura de devolución de llamada para recuperar la información de configuración actual de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e4de-109">Call the pfQueryInfo callback function in the callback structure to retrieve the current configuration information from the security database.</span></span>
3.  <span data-ttu-id="9e4de-110">Compare los valores:</span><span class="sxs-lookup"><span data-stu-id="9e4de-110">Compare the values:</span></span>

    -   <span data-ttu-id="9e4de-111">Si los datos difieren, llame a la función de devolución de llamada pfSetInfo en la estructura de devolución de llamada para actualizar los datos de configuración en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9e4de-111">If the data differs, call the pfSetInfo callback function in the callback structure to update the configuration data in the database.</span></span>
    -   <span data-ttu-id="9e4de-112">Si los datos son iguales, llame a la función de devolución de llamada pfSetInfo en la estructura de devolución de llamada para actualizar los datos de análisis en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9e4de-112">If the data is the same, call the pfSetInfo callback function in the callback structure to update the analysis data in the database.</span></span>

4.  <span data-ttu-id="9e4de-113">Repita el proceso hasta que se procesen todos los datos.</span><span class="sxs-lookup"><span data-stu-id="9e4de-113">Repeat until all data is processed.</span></span>

<span data-ttu-id="9e4de-114">En el ejemplo siguiente se muestra una posible implementación de [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md).</span><span class="sxs-lookup"><span data-stu-id="9e4de-114">The following example shows one possible implementation of [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md).</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo,
    IN SCESVC_CONFIGURATION_INFO *ServiceInfo
)
{
 
    ////////////////////////////////////////////////////
    // Define variables.
    ////////////////////////////////////////////////////
    SCESTATUS                      retCode;
    SCE_ENUMERATION_CONTEXT        EnumContext = 0;
    if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ||
         ServiceInfo == NULL ) 
    {
        return(SCESTATUS_INVALID_PARAMETER);
    }
  
  
    ////////////////////////////////////////////////////
    // Process supplied configuration information. 
    ////////////////////////////////////////////////////
    for (int i = 0; i < ServiceInfo->Count; i++)
    {
        retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              ServiceInfo->Line[I].Key,
                              TRUE,
                              (PVOID *)&pConfigInfo,
                              &EnumContext
                              );
        if(retCode != SCESTATUS_SUCCESS && 
           retCode != SCESTATUS_RECORD_NOT_FOUND)
        {
            ////////////////////////////////////////////////
            // Add code to handle errors
            ////////////////////////////////////////////////
            break;
        }
    
        //////////////////////////////////////////////////
        // If the supplied key is NULL, delete corresponding
        // key from configuration information and update 
        // analysis information if needed.
        //////////////////////////////////////////////////
        if(ServiceInfo->Line[I].Value == NULL)
        {
            if(retCode == SCESTATUS_SUCCESS)
            {
                EnumContext = 0;
                retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                          SceSvcAnalysisInfo,
                                          ServiceInfo->Line [i].Key,
                                          TRUE,
                                          (PVOID *)&pAnalInfo,
                                          &EnumContext
                                          );
                if(retCode == SCESTATUS_RECORD_NOT_FOUND)
                {
                  ////////////////////////////////////////////
                  // Analysis information for key was not found.
                  // Update analysis information to include 
                  // deleted key.
                  /////////////////////////////////////////////
                  UpdateInfo->Count = 1;
                  UpdateInfo->Line = &UpdateLine;
                  UpdateLine.Key = pConfigInfo->Line[0].Key;
                  UpdateLine.Value = (PBYTE)pConfigInfo->Line[0].Value;
                  retCode = (*(pSceCbInfo->pfSetInfo))( pSceCbInfo->sceHandle,
                                          SceSvcAnalysisInfo,
                                          NULL,
                                          TRUE,
                                          &UpdateInfo
                                          );
                  if(retCode != SCESTATUS_SUCCESS)
                  {
                    //////////////////////////////////////////
                    // Add code for error return codes.
                    //////////////////////////////////////////
                  } 
                }
                else if (retCode == SCESTATUS_SUCCESS)
                {
                 ////////////////////////////////////////////
                 // Add code to delete configuration (analysis
                 // information is already in place.
                 ////////////////////////////////////////////
                }
                else
                {
                  //////////////////////////////////////////
                  // Add code for error return codes.
                  //////////////////////////////////////////
                }
            
                //////////////////////////////////////////////
                // Delete key.
                //////////////////////////////////////////////
                retCode = (*(pSceCbInfo->pfSetInfo))( pSceCbInfo->sceHanlde,
                                        SceSvcConfigurationInfo,
                                        ServiceInfo->Line[I].Key,
                                        TRUE,
                                        NULL
                                        );
                if(retCode != SCESTATUS_SUCCESS)
                {
                  //////////////////////////////////////////
                  // Add code for error return codes.
                  //////////////////////////////////////////
                }
      
            }
            else
            {
                 /////////////////////////////////////////////////
                 // Supplied value is non-NULL; therefore. compare
                 // with current analysis information. If both are
                 // the same, delete current analysis. If they are 
                 // not the same, update security database with new
                 // value.
                 //////////////////////////////////////////
             
            }
   
   
           //////////////////////////////////////////////////
           // Free data returned.
           /////////////////////////////////////////////////
         (*(pSceCbInfo->pfFreeInfo))(pConfigInfo);
           pConfigInfo = NULL;
           
         (*(pSceCbInfo->pfSetInfo))(pAnalInfo);
           pAnalInfo = NULL;
          
          
          ////////////////////////////////////////////////////
          // Add code for other return codes if retCode is 
          // not SCESTATUS_SUCCESS.
          ///////////////////////////////////////////////////
          return retCode;
        }
    }
}
```



 

 



