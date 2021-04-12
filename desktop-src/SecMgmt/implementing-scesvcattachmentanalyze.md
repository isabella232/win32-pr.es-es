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
# <a name="implementing-scesvcattachmentanalyze"></a>Implementación de SceSvcAttachmentAnalyze

La función [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) debe recuperar la información de configuración de la base de datos de seguridad y el servicio, comparar los dos conjuntos de información y, a continuación, actualizar la sección de análisis de la base de datos de seguridad con cualquier diferencia. Puede asegurarse de esto mediante el siguiente algoritmo.

**Para implementar SceSvcAttachmentAnalyze**

1.  Defina las variables necesarias para recuperar y establecer la información de seguridad y los códigos de retorno.
2.  Llame a la función de devolución de llamada pfQueryInfo en la estructura de devolución de llamada para recuperar información de configuración de la base de datos de seguridad.
3.  Recupere la información correspondiente del servicio.
4.  Compare los datos de configuración recuperados del servicio con que se recuperaron de la base de datos de seguridad.
5.  Si la información no es igual, llame a la función de devolución de llamada pfSetInfo en la estructura de devolución de llamada para actualizar la base de datos.
6.  Libere todos los búferes utilizados para recuperar información. Llame a la función de devolución de llamada pfFreeInfo en la estructura de devolución de llamada para liberar la memoria usada para la información de base de datos devuelta.
7.  Si hay algún mensaje que la extensión desee agregar al archivo de registro de análisis, llame a la función de devolución de llamada pfLogInfo en la estructura de devolución de llamada.
8.  Devuelve los códigos de **SCESTATUS** apropiados.

En el ejemplo siguiente se muestra una posible implementación de [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md). Tenga en cuenta que en este ejemplo, las funciones QueryConfigurationLine y CompareValue consultan respectivamente la información del servicio y comparan esos valores con los recuperados de la base de datos de seguridad. No se muestra la implementación de estas funciones.


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



 

 



