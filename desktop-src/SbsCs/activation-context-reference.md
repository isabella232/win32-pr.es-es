---
description: Las funciones y estructuras de contexto de activación se usan con ensamblados en paralelo.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Referencia de contexto de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f8225b4db8b22227edf2b779ed9e1b50da7a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082615"
---
# <a name="activation-context-reference"></a>Referencia de contexto de activación

Las funciones y estructuras de contexto de activación se usan con ensamblados en paralelo.

En la tabla siguiente se enumeran las funciones de contexto de activación.



| Función                                                   | Descripción                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Activa el contexto de activación especificado.                                                                                                             |
| [**AddRefActCtx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Incrementa el recuento de referencias del contexto de activación especificado.                                                                                     |
| [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Crea un contexto de activación.                                                                                                                          |
| [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Desactiva el contexto de activación especificado.                                                                                                           |
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Devuelve los datos contenidos en la estructura de datos con clave de la [**\_ sección \_ \_ ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) que corresponde al GUID especificado.   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Devuelve los datos contenidos en la estructura de datos con clave de la [**\_ sección \_ \_ ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) que corresponde a la cadena especificada. |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Devuelve el contexto de activación actual.                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Garantiza que la memoria se libera cuando se carga, descarga y recarga un manifiesto.                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Consulta el contexto de activación para obtener información sobre un ensamblado o un archivo.                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Especifica el espacio de nombres y el nombre de atributo del atributo que se va a consultar.                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Disminuye el recuento de referencias del contexto de activación especificado.                                                                                     |
| [**ZombifyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Desactiva el contexto de activación especificado, pero no lo desasigna.                                                                               |



 

En la tabla siguiente se enumeran las estructuras de contexto de activación.



| Estructura                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ información detallada del ensamblado de contexto de \_ activación \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Contiene información detallada sobre el contexto de activación.                                                                                                                                                                                                                                                                                                                                  |
| [**\_ \_ información detallada del contexto de activación \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Contiene información sobre el ensamblado en el contexto de activación.                                                                                                                                                                                                                                                                                                                           |
| [**\_Índice de \_ consulta de contexto de activación \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Contiene el ensamblado en el contexto de activación y el índice del archivo dentro del ensamblado.                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Contiene información que describe un contexto de activación específico.                                                                                                                                                                                                                                                                                                                           |
| [**datos con clave de la \_ sección ACTCTX \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Devuelve la información de contexto de activación junto con el GUID o la sección de contexto de activación con etiqueta de entero de 32 bits.                                                                                                                                                                                                                                                                   |
| [**\_ \_ información detallada del archivo de ensamblado \_**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Contiene información sobre un archivo del ensamblado en el contexto de activación.                                                                                                                                                                                                                                                                                                                 |
| [**\_información del \_ nivel de ejecución del contexto de activación \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Lo utiliza la función [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2003 y Windows XP:** Esta estructura no está disponible.<br/>                                                                                                                                                                                                                                    |
| [**\_elemento de contexto de compatibilidad \_**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Lo utiliza la función [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) como parte de la estructura de información de compatibilidad del contexto de [**activación \_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) . <br/> **Windows Server 2008 y versiones anteriores, y Windows Vista y versiones anteriores:** Esta estructura no está disponible. Está disponible a partir de Windows Server 2008 R2 y Windows 7.<br/> |
| [**\_información de \_ compatibilidad del contexto de activación \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Lo utiliza la función [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2008 y versiones anteriores, y Windows Vista y versiones anteriores:** Esta estructura no está disponible. Está disponible a partir de Windows Server 2008 R2 y Windows 7.<br/>                                                                                                                                   |



 

En la tabla siguiente se enumeran las enumeraciones de contexto de activación.

| Enumeración                                                                       | Descripción                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACTCTX \_ \_ nivel de ejecución solicitado \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Describe el nivel de ejecución solicitado del contexto de activación. **Windows Server 2003 y Windows XP:** Esta enumeración no está disponible.<br/>                                                                                                      |
| [**\_tipo de \_ elemento de compatibilidad ACTCTX \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Describe el elemento Compatibility en el manifiesto de aplicación. **Windows Server 2008 y versiones anteriores, y Windows Vista y versiones anteriores:** Esta enumeración no está disponible. Está disponible a partir de Windows Server 2008 R2 y Windows 7.<br/> |



 

 

