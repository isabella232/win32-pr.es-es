---
description: Muestra los miembros de la clase CXAPOBase.
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: Miembros de CXAPOBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e76e1846b5dd9c28bec4f5cfe8e0168f5afbca012459b5860c4a5e23c610f6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962744"
---
# <a name="cxapobase-members"></a>Miembros de CXAPOBase

Muestra los miembros de la [**clase CXAPOBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)

## <a name="public-constructors"></a>Constructores públicos



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | Construye un [**objeto CXAPOBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) |



 

## <a name="public-methods"></a>Métodos públicos



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                   | Incrementa el recuento de referencias del objeto XAPO.<br/>                                                                                                         |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                     | Devuelve el número de fotogramas de entrada necesarios para generar el número especificado de fotogramas de salida.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                   | Devuelve el número de fotogramas de salida necesarios para generar el número especificado de fotogramas de entrada.<br/>                                                            |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo) | Devuelve las propiedades de registro de un XAPO.<br/>                                                                                                       |
| [**Inicializar**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (se hereda de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                               | Realiza cualquier inicialización específica del efecto.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (se hereda de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)       | Consulta si se admite un formato de entrada específico para un formato de salida determinado.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)     | Consulta si se admite un formato de salida específico para un formato de entrada determinado.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                       | Notifica a XAPO los formatos de [**secuencia**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que se van a dar al proceso.<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (se hereda de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                   | Recupera el puntero de interfaz solicitado si XAPO lo admite.<br/>                                                                                    |
| [**Versión**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (heredada de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                 | Disminuye el recuento de referencias del objeto XAPO y elimina el objeto si el recuento de referencias cae a cero.<br/>                                             |
| [**Restablecer**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (se hereda de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                         | Devuelve el objeto al estado en el que estaba justo después de llamar a [**LockForProcess.**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)<br/>                             |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                   | Opuesto a LockForProcess: las variables asignadas [**durante LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) se deben desasignar en este método.<br/> |



 

## <a name="protected-methods"></a>Métodos protegidos



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRegistrationPropertiesInternal**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | Devuelve un puntero a la estructura [**XAPO \_ REGISTRATION \_ PROPERTIES**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)S que contiene las propiedades de registro con las que se creó el XAPO.<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | Comprueba si el XAPO está bloqueado.<br/>                                                                                                                                                |
| LONG m \_ lReferenceCount<br/>                                                       | Recuento de referencias COM del objeto XAPO.<br/>                                                                                                                                       |
| [**ProcessThru**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | Lo llama una [**implementación IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) cuando un XAPO está deshabilitado para el procesamiento a través de .<br/>                                                  |
| [**ValidateFormatDefault**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | Comprueba que un formato de audio se encuentra dentro de los intervalos predeterminados admitidos.<br/>                                                                                                     |
| [**ValidateFormatPair**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | Comprueba que se admite una configuración de par de formato de entrada y salida con respecto a las marcas de propiedades XAPO.<br/>                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CXAPOBase (clase)**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
