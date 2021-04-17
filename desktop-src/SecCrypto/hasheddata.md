---
description: Proporciona funcionalidad para aplicar un algoritmo hash a una cadena.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Objeto HashedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670573"
---
# <a name="hasheddata-object"></a>Objeto HashedData

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase HashAlgorithm**](/previous-versions/windows/) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto **HashedData** proporciona funcionalidad para aplicar un algoritmo hash a una cadena.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **HashedData** se usa para realizar las siguientes tareas:

-   Especifique la cadena de contenido que contiene los datos a los que se va a aplicar un algoritmo hash.
-   Aplique un algoritmo hash especificado a la cadena de contenido.

## <a name="members"></a>Miembros

El objeto **HashedData** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **HashedData** tiene estos métodos.



| Método                          | Descripción                                        |
|:--------------------------------|:---------------------------------------------------|
| [**LM**](hasheddata-hash.md) | Crea un hash de la cadena especificada.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **HashedData** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso           | Descripción                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](hasheddata-algorithm.md)<br/> | Lectura/escritura<br/> | Establece o recupera el tipo de algoritmo hash que se usa.<br/>                                                                                                                     |
| [**Value**](hasheddata-value.md)<br/>         | Solo lectura<br/>  | Recupera los datos a los que se ha aplicado un algoritmo hash después de llamar correctamente al método [**hash**](hasheddata-hash.md) . El hash se devuelve en formato hexadecimal. Esta es la propiedad predeterminada.<br/> |



 

## <a name="remarks"></a>Observaciones

Para crear el hash de una gran cantidad de datos, llame al método [**hash**](hasheddata-hash.md) para cada fragmento de datos. El hash de cada fragmento de datos se concatena a la propiedad [**Value**](hasheddata-value.md) hasta que se lee la propiedad. El contenido de la propiedad **Value** se restablece cuando se lee la propiedad.

Se puede crear el objeto **HashedData** y es seguro para el scripting. El identificador de programa (ProgID) del objeto **HashedData** es "CAPICOM. HashedData. 1 ".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
