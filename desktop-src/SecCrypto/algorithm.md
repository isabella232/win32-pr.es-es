---
description: Especifica el algoritmo utilizado para la firma, la envoltura y las operaciones de cifrado.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Objeto Algorithm (CAPICOM. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670393"
---
# <a name="algorithm-object"></a>Algorithm (objeto)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto **algorithm** especifica el algoritmo utilizado para la firma, la envoltura y las operaciones de cifrado.

## <a name="when-to-use"></a>Cuándo se usa

El objeto de **algoritmo** se usa para realizar las siguientes tareas:

-   Establezca o recupere el algoritmo que se va a usar.
-   Establezca o recupere la longitud de la clave.

> [!Note]  
> CAPICOM intenta usar el proveedor de servicios criptográficos (CSP) predeterminado del sistema. Si ese CSP no puede proporcionar la longitud de clave o el algoritmo solicitado, CAPICOM busca un CSP proporcionado por Microsoft que pueda controlar el algoritmo y la longitud de clave solicitados, en este orden de disponibilidad: proveedor de servicios criptográficos mejorados de Microsoft, proveedor de servicios criptográficos seguros de Microsoft, proveedor de servicios criptográficos básicos de Microsoft.

 

## <a name="members"></a>Miembros

El objeto **algorithm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **algoritmo** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso           | Descripción                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength**](algorithm-keylength.md)<br/> | Lectura/escritura<br/> | Establece o recupera la longitud de la clave.<br/>                                                                               |
| [**Name**](algorithm-name.md)<br/>           | Lectura/escritura<br/> | Establece o recupera el algoritmo utilizado para la firma, la envoltura y el cifrado de las operaciones. Esta es la propiedad predeterminada.<br/> |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto de **algoritmo** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Encabezado<br/>                | <dl> <dt>CAPICOM. h</dt> </dl>   |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
