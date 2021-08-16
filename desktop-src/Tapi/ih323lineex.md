---
description: La interfaz IH323LineEx se implementa mediante el MSP H323 y solo está disponible en objetos de dirección H.323. Esta interfaz expone métodos que permiten la creación y manipulación de terminales que pueden comunicarse entre clientes H323 y SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interfaz IH323LineEx (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 856deae92568acd2eb9f9394e949dc2d5ea6a4bbde9c2c28f0b998c99098eef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013115"
---
# <a name="ih323lineex-interface"></a>Interfaz IH323LineEx

\[**IH323LineEx** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz IH323LineEx** se implementa mediante el [MSP H323](h323-msp.md) y solo está disponible en objetos de dirección H.323. Esta interfaz expone métodos que permiten la creación y manipulación de terminales que pueden comunicarse entre clientes H323 y SDP.

> [!Note]  
> Solo se debe llamar a todos los métodos de esta interfaz después de registrarse para las llamadas entrantes en esta dirección.

 

## <a name="members"></a>Miembros

La **interfaz IH323LineEx** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IH323LineEx** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IH323LineEx** tiene estos métodos.



| Método                                                                                 | Descripción                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**SetAlias**](ih323lineex-setalias.md)                                               | Configura un alias H.323 predeterminado para la dirección.<br/>             |
| [**SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md) | Configura la ponderación de preferencias para las funcionalidades predeterminadas.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Configura una dirección T.120 externa para el intercambio de datos.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

