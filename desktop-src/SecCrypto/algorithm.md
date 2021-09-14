---
description: Especifica el algoritmo utilizado para firmar, envolver y cifrar operaciones.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Objeto Algorithm (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173298"
---
# <a name="algorithm-object"></a>Objeto algorithm

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto Algorithm** especifica el algoritmo utilizado para firmar, envolver y cifrar operaciones.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Algorithm** se usa para realizar las siguientes tareas:

-   Establezca o recupere el algoritmo que se va a usar.
-   Establezca o recupere la longitud de la clave.

> [!Note]  
> CAPICOM intenta usar el proveedor de servicios criptográficos (CSP) predeterminado del sistema. Si ese CSP no puede proporcionar el algoritmo o la longitud de clave solicitados, CAPICOM busca un CSP proporcionado por Microsoft disponible que pueda controlar el algoritmo y la longitud de clave solicitados, en este orden de disponibilidad: Proveedor de servicios criptográficos mejorados de Microsoft, Proveedor de servicios criptográficos seguros de Microsoft y Proveedor criptográfico base de Microsoft.

 

## <a name="members"></a>Members

El **objeto Algorithm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Algorithm** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso           | Descripción                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength**](algorithm-keylength.md)<br/> | Lectura y escritura<br/> | Establece o recupera la longitud de la clave.<br/>                                                                               |
| [**Nombre**](algorithm-name.md)<br/>           | Lectura y escritura<br/> | Establece o recupera el algoritmo utilizado para firmar, envolver y cifrar operaciones. Esta es la propiedad predeterminada.<br/> |



 

## <a name="remarks"></a>Observaciones

No **se puede** crear el objeto Algorithm.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Encabezado<br/>                | <dl> <dt>Capicom.h</dt> </dl>   |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
