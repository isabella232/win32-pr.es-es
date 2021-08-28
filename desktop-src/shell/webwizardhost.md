---
description: Expone métodos que permiten que las páginas HTML hospedadas en una extensión del asistente se comuniquen con el asistente.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Objeto WebWizardHost (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: c5bcf40a77c2f464d5277ac4823ed74a3f3c2bdd6a2114d2431684cc8b319f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967754"
---
# <a name="webwizardhost-object"></a>Objeto WebWizardHost

Expone métodos que permiten que las páginas HTML hospedadas en una extensión del asistente se comuniquen con el asistente.

## <a name="members"></a>Miembros

El **objeto WebWizardHost** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto WebWizardHost** tiene estos métodos.



| Método                                                      | Descripción                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cancelar**](iwebwizardhost-cancel.md)                     | Simula un clic **en el** botón Cancelar.<br/>                                                                                                                                    |
| [**FinalBack**](iwebwizardhost-finalback.md)               | Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.<br/>                                                                    |
| [**FinalNext**](iwebwizardhost-finalnext.md)               | Navega a la página del asistente del lado cliente que sigue a la página que hospeda las páginas HTML del lado servidor o finaliza el asistente si no hay más páginas del lado cliente.<br/> |
| [**SetHeaderText**](iwebwizardhost-setheadertext.md)       | Establece el título y el subtítulo que aparecen en el encabezado del asistente. En general, el cliente mostrará el encabezado encima del CÓDIGO HTML y debajo de la barra de título.<br/>                    |
| [**SetWizardButtons**](iwebwizardhost-setwizardbuttons.md) | Actualiza los **botones** **Atrás,** Siguiente **y** Finalizar en el marco del asistente del cliente.<br/>                                                                                    |



 

### <a name="properties"></a>Propiedades

El **objeto WebWizardHost** tiene estas propiedades.



| Propiedad                                               | Tipo de acceso           | Descripción                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Caption**](iwebwizardhost-caption.md)<br/>   | Lectura/escritura<br/> | Sin implementar.<br/>                              |
| [**Propiedad**](iwebwizardhost-property.md)<br/> | Lectura/escritura<br/> | Establece o recupera el valor actual de una propiedad.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |
| IID<br/>                      | CLSID \_ WebWizardHost<br/>                                                        |



 

 




