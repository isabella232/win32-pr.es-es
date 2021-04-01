---
description: Muestra los miembros de la clase CXAPOBase.
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: Miembros de CXAPOBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab63cf7e8ac6e4d0fa14ec412b53682aff2ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082955"
---
# <a name="cxapobase-members"></a>Miembros de CXAPOBase

Muestra los miembros de la clase [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

## <a name="public-constructors"></a>Constructores públicos



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | Construye un objeto [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) . |



 

## <a name="public-methods"></a>Métodos públicos



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (heredado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                   | Incrementa el recuento de referencias del objeto XAPO.<br/>                                                                                                         |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                     | Devuelve el número de fotogramas de entrada necesarios para generar el número dado de fotogramas de salida.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Devuelve el número de fotogramas de salida necesarios para generar el número especificado de fotogramas de entrada.<br/>                                                            |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)) | Devuelve las propiedades de registro de un XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                               | Realiza cualquier inicialización específica del efecto.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Consulta si se admite un formato de entrada específico para un formato de salida determinado.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))     | Consulta si se admite un formato de salida específico para un formato de entrada determinado.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                       | Notifica a XAPO que se proporcionará el [**proceso**](/windows/win32/api/xapo/nf-xapo-ixapo-process) de formatos de flujo.<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Recupera el puntero de interfaz solicitado Si el XAPO lo admite.<br/>                                                                                    |
| [**Release**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                 | Disminuye el recuento de referencias del objeto XAPO y elimina el objeto si el recuento de referencias llega a cero.<br/>                                             |
| [**Restablecer**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (heredado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Devuelve el objeto al estado en el que se encontraba justo después de llamar a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Contraria a LockForProcess: las variables asignadas durante [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) deben desasignarse en este método.<br/> |



 

## <a name="protected-methods"></a>Métodos protegidos



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRegistrationPropertiesInternal**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | Devuelve un puntero a la estructura de [**\_ \_ propiedades de registro de XAPO**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)que contiene las propiedades de registro con las que se creó XAPO.<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | Comprueba si el XAPO está bloqueado.<br/>                                                                                                                                                |
| LONG m \_ lReferenceCount<br/>                                                       | Recuento de referencias COM del objeto XAPO.<br/>                                                                                                                                       |
| [**ProcessThru**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | Llamado por una implementación de [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) cuando un XAPO está deshabilitado para el procesamiento.<br/>                                                  |
| [**ValidateFormatDefault**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | Comprueba que un formato de audio se encuentra dentro de los intervalos predeterminados admitidos.<br/>                                                                                                     |
| [**ValidateFormatPair**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | Comprueba que se admite una configuración de par de formato de entrada y salida con respecto a las marcas de propiedad XAPO.<br/>                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Clase CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
