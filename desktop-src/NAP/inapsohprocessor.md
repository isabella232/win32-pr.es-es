---
title: Interfaz INapSoHProcessor (NapProtocol. h)
description: Los Sha usan para procesar el contenido de SoHResponses y de los SHV para procesar el contenido de SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- Interfaz INapSoHProcessor NAP
- Interfaz INapSoHProcessor NAP, descripción
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
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078896"
---
# <a name="inapsohprocessor-interface"></a>Interfaz INapSoHProcessor

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapSoHProcessor** proporciona métodos que los Sha usan para procesar el contenido de [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) y SHV para procesar el contenido de **SoHRequests**.

## <a name="members"></a>Miembros

La interfaz **INapSoHProcessor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSoHProcessor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapSoHProcessor** tiene estos métodos.



| Método                                                                                           | Descripción                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)         | Busca el índice de ubicación del siguiente atributo de paquete SoH.<br/>                 |
| [**INapSoHProcessor:: GetAttribute**](inapsohprocessor-getattribute-method.md)                   | Recupera el tipo y el valor del atributo.<br/>                                    |
| [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md) | Recupera el número de atributos contenidos en el SoH.<br/>                   |
| [**INapSoHProcessor:: Initialize**](inapsohprocessor-initialize-method.md)                       | Inicializa el paquete de protocolo SoH y el sistema NAP para el procesamiento de contenido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

