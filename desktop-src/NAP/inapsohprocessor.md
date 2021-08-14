---
title: Interfaz INapSoHProcessor (NapProtocol.h)
description: Las SHA usan para procesar el contenido de SoHResponses y los SHV para procesar el contenido de SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- NAP de interfaz INapSoHProcessor
- Nap de interfaz INapSoHProcessor , descrito
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca4a87e15d3810605038231eaec066e9f26ed079aca0d0715c72e7c69ed8d600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799487"
---
# <a name="inapsohprocessor-interface"></a>Interfaz INapSoHProcessor

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSoHProcessor** proporciona métodos que usan los SHA para procesar el contenido de [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) y los SHV para procesar el contenido de **SoHRequests.**

## <a name="members"></a>Miembros

La **interfaz INapSoHProcessor** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSoHProcessor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapSoHProcessor** tiene estos métodos.



| Método                                                                                           | Descripción                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)         | Busca el índice de ubicación del siguiente atributo de paquete SoH.<br/>                 |
| [**INapSoHProcessor::GetAttribute**](inapsohprocessor-getattribute-method.md)                   | Recupera el tipo de atributo y el valor.<br/>                                    |
| [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md) | Recupera el número de atributos contenidos en el SoH.<br/>                   |
| [**INapSoHProcessor::Initialize**](inapsohprocessor-initialize-method.md)                       | Inicializa el paquete de protocolo SoH y el sistema NAP para el procesamiento de contenido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

