---
description: Muestra los miembros de la clase CXAPOParametersBase.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: Miembros de CXAPOParametersBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e225d1628408b5d5472bed8c3060f714bb7b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716381"
---
# <a name="cxapoparametersbase-members"></a>Miembros de CXAPOParametersBase

Muestra los miembros de la clase [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

## <a name="public-constructors"></a>Constructores públicos



|                                                    |                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Construye un objeto [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) . |



 

## <a name="public-methods"></a>Métodos públicos



|                                                                                                                              |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (heredado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Incrementa el recuento de referencias del objeto XAPO.<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Devuelve los parámetros de proceso actuales. <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                           | Devuelve el número de fotogramas de entrada necesarios para generar el número dado de fotogramas de salida.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Devuelve el número de fotogramas de salida necesarios para generar el número especificado de fotogramas de entrada.<br/>                                                            |
| [**EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Notifica a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) que XAPO ha finalizado el acceso a los parámetros de proceso actuales. <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (heredado de [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Obtiene los parámetros específicos del efecto. <br/>                                                                                                                     |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Devuelve las propiedades de registro de un XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                     | Realiza cualquier inicialización específica del efecto.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))             | Consulta si se admite un formato de entrada específico para un formato de salida determinado.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))           | Consulta si se admite un formato de salida específico para un formato de entrada determinado.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                             | Notifica a XAPO que se proporcionará el [**proceso**](/windows/win32/api/xapo/nf-xapo-ixapo-process) de formatos de flujo.<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Lo llama [**IXAPOParameters:: SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) para permitir la validación de parámetros definidos por el usuario. <br/>          |
| [**ParametersChanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Indica si se ha llamado a [**IXAPOParameters:: SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) desde la última fase de procesamiento. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Recupera el puntero de interfaz solicitado Si el XAPO lo admite.<br/>                                                                                    |
| [**Release**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                       | Disminuye el recuento de referencias del objeto XAPO y elimina el objeto si el recuento de referencias llega a cero.<br/>                                             |
| [**Restablecer**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (heredado de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                               | Devuelve el objeto al estado en el que se encontraba justo después de llamar a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (se hereda de [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Establece parámetros específicos del efecto.<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (se hereda de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Contraria a LockForProcess: las variables asignadas durante [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) deben desasignarse en este método.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Clase CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
