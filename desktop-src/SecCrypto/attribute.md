---
description: Representa un único atributo autenticado.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute, objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671631"
---
# <a name="attribute-object"></a>Attribute, objeto

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]

El objeto de **atributo** representa un único atributo autenticado.

## <a name="when-to-use"></a>Cuándo se usa

El objeto de **atributo** se usa para realizar las siguientes tareas:

-   Establezca o recupere el nombre de CAPICOM del atributo.
-   Establezca o recupere el valor del atributo, como la hora de la firma, el nombre del documento firmado o una descripción del documento firmado.

## <a name="members"></a>Miembros

El objeto de **atributo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **atributo** tiene estas propiedades.



| Propiedad                                    | Tipo de acceso           | Descripción                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Name**](attribute-name.md)<br/>   | Lectura/escritura<br/> | Establece o recupera el nombre de CAPICOM del atributo. Esta es la propiedad predeterminada.<br/> |
| [**Value**](attribute-value.md)<br/> | Lectura/escritura<br/> | Establece o recupera el valor del atributo.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto de **atributo** y es seguro para el scripting. El ProgID del objeto de **atributo** es CAPICOM. Attribute. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
