---
description: Muestra los miembros de la clase CXAPOParametersBase.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: CXAPOParametersBase Members
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554aa66b4166bc3d0de4db685e0f6e7b54e6ebf5
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423875"
---
# <a name="cxapoparametersbase-members"></a>CXAPOParametersBase Members

Muestra los miembros de la [**clase CXAPOParametersBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)

## <a name="public-constructors"></a>Constructores públicos



|    Constructor                                                |     Descripción                                                                    |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Construye un [**objeto CXAPOParametersBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) |



 

## <a name="public-methods"></a>Métodos públicos



|        Método                                                                                                                      |     Descripción                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                         | Incrementa el recuento de referencias del objeto XAPO.<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Devuelve los parámetros de proceso actuales. <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                           | Devuelve el número de fotogramas de entrada necesarios para generar el número especificado de fotogramas de salida.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Devuelve el número de fotogramas de salida necesarios para generar el número especificado de fotogramas de entrada.<br/>                                                            |
| [**EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Notifica a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) que XAPO ha terminado de acceder a los parámetros de proceso actuales. <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (heredado de [**IXAPOParameters)**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) | Obtiene parámetros específicos del efecto. <br/>                                                                                                                     |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)       | Devuelve las propiedades de registro de un XAPO.<br/>                                                                                                       |
| [**Inicializar**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (se hereda de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                     | Realiza cualquier inicialización específica del efecto.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (se hereda de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)             | Consulta si se admite un formato de entrada específico para un formato de salida determinado.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (se hereda de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)           | Consulta si se admite un formato de salida específico para un formato de entrada determinado.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                             | Notifica a XAPO los formatos de secuencia [**que**](/windows/win32/api/xapo/nf-xapo-ixapo-process) se darán al proceso.<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | [**IXAPOParameters::SetParameters llama**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) a para permitir la validación de parámetros definidos por el usuario. <br/>          |
| [**ParametersChanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Indica si se [**ha llamado a IXAPOParameters::SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) desde el último paso de procesamiento. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (se hereda de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Recupera el puntero de interfaz solicitado si el XAPO lo admite.<br/>                                                                                    |
| [**Versión**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (heredada de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                       | Disminuye el recuento de referencias del objeto XAPO y elimina el objeto si el recuento de referencias cae a cero.<br/>                                             |
| [**Restablecimiento**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                               | Devuelve el objeto al estado en el que estaba justo después de llamar a [**LockForProcess.**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (se hereda de [**IXAPOParameters)**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) | Establece parámetros específicos del efecto.<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (heredado de [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Opuesto a LockForProcess: las variables asignadas [**durante LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) se deben desasignar en este método.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CXAPOParametersBase (clase)**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
