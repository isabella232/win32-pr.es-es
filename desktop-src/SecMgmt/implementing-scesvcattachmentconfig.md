---
description: Debe recuperar información de la base de datos de seguridad y, a continuación, usar esa información para configurar el servicio.
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: Implementación de SceSvcAttachmentConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98eb519e6422e3036ddfb203811322befd2713
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374887"
---
# <a name="implementing-scesvcattachmentconfig"></a>Implementación de SceSvcAttachmentConfig

La [**función SceSvcAttachmentConfig**](scesvcattachmentconfig.md) debe recuperar información de la base de datos de seguridad y, a continuación, usar esa información para configurar el servicio.

Al implementar [**SceSvcAttachmentConfig,**](scesvcattachmentconfig.md)puede recuperar toda la información y, a continuación, configurar el servicio, o bien recuperar y configurar el servicio en pasos. El algoritmo siguiente recupera toda la información y, a continuación, configura el servicio.

**Para implementar SceSvcAttachmentConfig**

1.  Defina las variables necesarias para recuperar información y códigos de retorno.
2.  Llame a la función de devolución de llamada pfQueryInfo en la estructura de devolución de llamada para recuperar información de configuración de la base de datos de seguridad.
3.  Configure el sistema con la información devuelta.
4.  Llame a la función de devolución de llamada pfFreeInfo en la estructura de devolución de llamada para liberar la memoria usada para la información devuelta.
5.  Si hay algún mensaje que la extensión desea agregar al archivo de registro de análisis, llame a la función de devolución de llamada pfLogInfo en la estructura de devolución de llamada.
6.  Devuelve los códigos **SCESTATUS adecuados.**

En el ejemplo siguiente se muestra una posible implementación de [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md). Tenga en cuenta que en este ejemplo, la función ProcessConfigurationLine establece la configuración del servicio. No se muestra la implementación de esta función.


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



 

 



