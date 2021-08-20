---
description: El objeto ConfigureModule es una interfaz implementada por el cliente.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Objeto ConfigureModule (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7685ce1f1c9c7d8f519395c578000375742eea49dd169085e99c582e14c35a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143723"
---
# <a name="configuremodule-object"></a>Objeto ConfigureModule

El **objeto ConfigureModule** es una interfaz implementada por el cliente. Mergemod.dllllama a métodos en **la interfaz IMsmConfigureModule para** solicitar que la herramienta cliente proporcione información de configuración. El módulo se configura en función de las respuestas del cliente a las llamadas en esta interfaz.

## <a name="members"></a>Miembros

El **objeto ConfigureModule** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto ConfigureModule** tiene estos métodos.



| Método                                                           | Descripción                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**ProvideIntegerData**](configuremodule-provideintegerdata.md) | Llamado por Mergemod.dll para obtener los enteros usados para configurar el módulo.<br/> |
| [**ProvideTextData**](configuremodule-providetextdata.md)       | Llamado por Mergemod.dll para obtener el texto utilizado para configurar el módulo.<br/>     |



 

## <a name="remarks"></a>Comentarios

### <a name="c"></a>C++

interface **IMsmConfigureModule: IDispatch**

### <a name="interface-id"></a>Identificador de interfaz



| Constante                     | Value                                  |
|------------------------------|----------------------------------------|
| **IID \_ IMsmConfigureModule** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




