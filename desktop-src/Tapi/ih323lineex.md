---
description: El MSP de H323 implementa la interfaz IH323LineEx y solo está disponible en los objetos de dirección H. 323. Esta interfaz expone métodos que permiten la creación y la manipulación de terminales que pueden comunicarse entre clientes H323 y SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interfaz IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680526"
---
# <a name="ih323lineex-interface"></a>Interfaz IH323LineEx

\[**IH323LineEx** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El [MSP de H323](h323-msp.md) implementa la interfaz **IH323LineEx** y solo está disponible en los objetos de dirección H. 323. Esta interfaz expone métodos que permiten la creación y la manipulación de terminales que pueden comunicarse entre clientes H323 y SDP.

> [!Note]  
> Solo se debe llamar a todos los métodos de esta interfaz después de registrarse para las llamadas entrantes en esta dirección.

 

## <a name="members"></a>Miembros

La interfaz **IH323LineEx** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IH323LineEx** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IH323LineEx** tiene estos métodos.



| Método                                                                                 | Descripción                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**SetAlias**](ih323lineex-setalias.md)                                               | Configura un alias H. 323 predeterminado para la dirección.<br/>             |
| [**SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md) | Configura la ponderación de las preferencias para las funciones predeterminadas.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Configura una dirección T. 120 externa para el intercambio de datos.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

