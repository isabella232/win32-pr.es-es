---
description: Las funciones y estructuras del contexto de activación se usan con ensamblados en paralelo.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Referencia de contexto de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72eb4bc136a95766a62bb96e67ac198f88fca905c60ba98e6bf922ce65a36389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142588"
---
# <a name="activation-context-reference"></a>Referencia de contexto de activación

Las funciones y estructuras del contexto de activación se usan con ensamblados en paralelo.

En la tabla siguiente se enumeran las funciones de contexto de activación.



| Función                                                   | Descripción                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Activa el contexto de activación especificado.                                                                                                             |
| [**AddRefActCtx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Incrementa el recuento de referencias del contexto de activación especificado.                                                                                     |
| [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Crea un contexto de activación.                                                                                                                          |
| [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Desactiva el contexto de activación especificado.                                                                                                           |
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Devuelve los datos contenidos en la estructura DE DATOS KEYED DE LA [**\_ SECCIÓN \_ DE \_ ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) que corresponde al GUID especificado.   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Devuelve los datos contenidos en la estructura [**\_ ACTCTX SECTION \_ KEYED \_ DATA**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) que corresponde a la cadena especificada. |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Devuelve el contexto de activación actual.                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Garantiza que la memoria se libera cuando se carga, descarga y recarga un manifiesto.                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Consulta el contexto de activación para obtener información sobre un ensamblado o archivo.                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Especifica el espacio de nombres y el nombre del atributo que se va a consultar.                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Disminuye el recuento de referencias del contexto de activación especificado.                                                                                     |
| [**HexadecimalfyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Desactiva el contexto de activación especificado, pero no lo desasigna.                                                                               |



 

En la tabla siguiente se enumeran las estructuras de contexto de activación.



| Estructura                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMACIÓN DETALLADA \_ DEL ENSAMBLADO DE CONTEXTO DE \_ \_ \_ ACTIVACIÓN**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Contiene información detallada sobre el contexto de activación.                                                                                                                                                                                                                                                                                                                                  |
| [**INFORMACIÓN \_ DETALLADA DEL CONTEXTO DE \_ \_ ACTIVACIÓN**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Contiene información sobre el ensamblado en el contexto de activación.                                                                                                                                                                                                                                                                                                                           |
| [**ÍNDICE DE \_ CONSULTA DE CONTEXTO DE \_ \_ ACTIVACIÓN**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Contiene el ensamblado dentro del contexto de activación y el índice del archivo dentro del ensamblado.                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Contiene información que describe un contexto de activación específico.                                                                                                                                                                                                                                                                                                                           |
| [**DATOS CON CLAVE \_ DE SECCIÓN \_ DE ACTCTX \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Devuelve la información del contexto de activación junto con el GUID o la sección contexto de activación etiquetado con enteros de 32 bits.                                                                                                                                                                                                                                                                   |
| [**INFORMACIÓN \_ DETALLADA DEL ARCHIVO DE \_ \_ ENSAMBLADO**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Contiene información sobre un archivo del ensamblado en el contexto de activación.                                                                                                                                                                                                                                                                                                                 |
| [**INFORMACIÓN DE \_ NIVEL DE EJECUCIÓN DEL CONTEXTO DE \_ \_ \_ ACTIVACIÓN**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Usado por la [**función QueryActCtxW.**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)<br/> **Windows Server 2003 y Windows XP:** Esta estructura no está disponible.<br/>                                                                                                                                                                                                                                    |
| [**ELEMENTO DE \_ CONTEXTO DE \_ COMPATIBILIDAD**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Usado por la [**función QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) como parte de la estructura [**ACTIVATION CONTEXT COMPATIBILITY \_ \_ \_ INFORMATION.**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) <br/> **Windows Server 2008 y versiones anteriores, y Windows Vista y versiones anteriores:** Esta estructura no está disponible. Está disponible a partir de Windows Server 2008 R2 y Windows 7.<br/> |
| [**INFORMACIÓN DE \_ COMPATIBILIDAD DEL CONTEXTO DE \_ \_ ACTIVACIÓN**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Usado por la [**función QueryActCtxW.**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)<br/> **Windows Server 2008 y versiones anteriores, y Windows Vista y versiones anteriores:** Esta estructura no está disponible. Está disponible a partir de Windows Server 2008 R2 y Windows 7.<br/>                                                                                                                                   |



 

En la tabla siguiente se enumeran las enumeraciones de contexto de activación.

| Enumeración                                                                       | Descripción                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NIVEL DE EJECUCIÓN \_ SOLICITADO DE ACTCTX \_ \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Describe el nivel de ejecución solicitado del contexto de activación. **Windows Server 2003 y Windows XP:** Esta enumeración no está disponible.<br/>                                                                                                      |
| [**TIPO DE ELEMENTO \_ DE COMPATIBILIDAD \_ DE ACTCTX \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Describe el elemento de compatibilidad en el manifiesto de aplicación. **Windows Server 2008 y versiones anteriores, y Windows Vista y versiones anteriores:** Esta enumeración no está disponible. Está disponible a partir de Windows Server 2008 R2 y Windows 7.<br/> |



 

 

