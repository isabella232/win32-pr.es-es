---
title: asignar atributo
description: El atributo \ allocate \ ACF permite personalizar la asignación y desasignación de memoria para un tipo definido en el archivo IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- asignar el atributo MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904037"
---
# <a name="allocate-attribute"></a>asignar atributo

El atributo **\[ allocate \]** ACF permite personalizar la asignación y desasignación de memoria para un tipo definido en el archivo IDL.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de opciones de asignación* 
</dt> <dd>

Especifica una o más opciones de asignación de memoria. Seleccione uno de **los \_ nodos** de un **solo \_ nodo** o de todos, o de uno de ellos **gratis** o **no \_ libre**, o de uno de los pares. Al especificar más de una opción, separe las opciones con comas.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica otros atributos de tipo ACF opcionales. Al especificar más de un atributo de tipo, separe las opciones con comas.

</dd> <dt>

*nombre de tipo* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ allocate \]** tiene las siguientes opciones válidas.



| Opción           | Descripción                                                           |
|------------------|-----------------------------------------------------------------------|
| **todos los \_ nodos**   | Realiza una llamada a para asignar y liberar memoria para todos los nodos.             |
| **\_nodo único** | Realiza muchas llamadas individuales para asignar y liberar cada nodo de memoria. |
| **free**         | Libera memoria al volver del código auxiliar del servidor.                          |
| **no \_ gratis**   | No libera memoria al volver del código auxiliar del servidor.                  |



 

De forma predeterminada, el código auxiliar puede asignar almacenamiento para los datos a los que hace referencia un puntero único o completo mediante una llamada a la [**\_ \_ asignación de usuarios de MIDL**](midl-user-allocate-1.md) y el [**usuario de MIDL \_ \_**](midl-user-free-1.md) de forma individual para cada puntero.

Puede optimizar la velocidad de la aplicación especificando la opción **todos los \_ nodos**. Esta opción indica al código auxiliar que calcule el tamaño de toda la memoria a la que se hace referencia a través del puntero del tipo especificado y que realice una llamada única a la [**\_ \_ asignación de usuarios de MIDL**](midl-user-allocate-1.md). El código auxiliar libera la memoria realizando una llamada a la versión [**\_ \_ gratuita del usuario de MIDL**](midl-user-free-1.md).

La opción **no \_ Free** indica al compilador de MIDL que genere un código auxiliar de servidor que no llame al [**usuario de MIDL \_ \_ Free**](midl-user-free-1.md) para el tipo especificado. La opción **no \_ Free** permite que las estructuras de puntero sigan siendo accesibles para la aplicación de servidor después de que se haya completado la llamada a procedimiento remoto y se haya devuelto al cliente.

El atributo **\[ allocate \]** producirá cualquier parámetro **\[ in, out \]** que sea un puntero a un tipo calificado con la opción **All \_ Nodes** para reasignar la memoria cuando no se calculan las referencias de los datos. Es responsabilidad de la aplicación liberar la memoria asignada previamente para este parámetro. Por ejemplo:

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

El código auxiliar reasignará el tipo de datos PTHISTYPE antes de la anulación de [**\[ \]**](out-idl.md) la serialización. Por lo tanto, la aplicación debe liberar la memoria asignada previamente para los datos de este parámetro o se producirá una fuga de memoria.

## <a name="examples"></a>Ejemplos

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**\_asignación de usuarios de MIDL \_**](midl-user-allocate-1.md)
</dt> <dt>

[**usuario de MIDL \_ \_ gratis**](midl-user-free-1.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




