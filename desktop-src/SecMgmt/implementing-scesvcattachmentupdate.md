---
description: Toma como parámetro un conjunto de información de configuración proporcionada.
ms.assetid: 3c0a71f6-f643-4a5e-8b5c-15c976a3736e
title: Implementación de SceSvcAttachmentUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f2399ee87fdc97dcfb82d9fd711c6407894c3dbbbf17a31df39bb225010032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894599"
---
# <a name="implementing-scesvcattachmentupdate"></a>Implementación de SceSvcAttachmentUpdate

La [**función SceSvcAttachmentUpdate**](scesvcattachmentupdate.md) toma como parámetro un conjunto de información de configuración proporcionada. A continuación, recupera información de la base de datos de seguridad, calcula una nueva configuración base mediante la información de configuración proporcionada, calcula la nueva información de análisis basada en la información de base de datos y la información de configuración proporcionada, y actualiza la base de datos con la nueva configuración base e información de análisis. Puede implementar **SceSvcAttachmentUpdate** mediante el algoritmo siguiente.

**Para implementar SceSvcAttachmentUpdate**

1.  Defina las variables necesarias para recuperar información, establecer información y códigos de retorno.
2.  Llame a la función de devolución de llamada pfQueryInfo en la estructura de devolución de llamada para recuperar la información de configuración actual de la base de datos de seguridad.
3.  Compare los valores:

    -   Si los datos difieren, llame a la función de devolución de llamada pfSetInfo en la estructura de devolución de llamada para actualizar los datos de configuración de la base de datos.
    -   Si los datos son los mismos, llame a la función de devolución de llamada pfSetInfo en la estructura de devolución de llamada para actualizar los datos de análisis de la base de datos.

4.  Repita la repetición hasta que se procese todos los datos.

En el ejemplo siguiente se muestra una posible implementación de [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md).


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



 

 



