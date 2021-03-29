---
description: El objeto ConfigureModule es una interfaz implementada por el cliente.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Objeto ConfigureModule (Mergemod. h)
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
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653923"
---
# <a name="configuremodule-object"></a>Objeto ConfigureModule

El **objeto ConfigureModule** es una interfaz implementada por el cliente. Mergemod.dllllama a los métodos de la interfaz **IMsmConfigureModule** para solicitar que la herramienta cliente proporcione información de configuración. El módulo se configura en función de las respuestas del cliente a las llamadas en esta interfaz.

## <a name="members"></a>Miembros

El objeto **ConfigureModule** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **ConfigureModule** tiene estos métodos.



| Método                                                           | Descripción                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**ProvideIntegerData**](configuremodule-provideintegerdata.md) | Llamado por Mergemod.dll para obtener enteros utilizados para configurar el módulo.<br/> |
| [**ProvideTextData**](configuremodule-providetextdata.md)       | Llamado por Mergemod.dll para obtener el texto que se usa para configurar el módulo.<br/>     |



 

## <a name="remarks"></a>Observaciones

### <a name="c"></a>C++

interfaz **IMsmConfigureModule: IDispatch**

### <a name="interface-id"></a>IDENTIFICADOR de interfaz



| Constante                     | Value                                  |
|------------------------------|----------------------------------------|
| **\_IMSMCONFIGUREMODULE IID** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




