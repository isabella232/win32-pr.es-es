---
title: atributo allocate
description: El atributo \ allocate\ ACF permite personalizar la asignación y desasignación de memoria para un tipo definido en el archivo IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- allocate attribute MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159688"
---
# <a name="allocate-attribute"></a>atributo allocate

El **\[ atributo allocate \]** ACF permite personalizar la asignación y desasignación de memoria para un tipo definido en el archivo IDL.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*allocate-option-list* 
</dt> <dd>

Especifica una o varias opciones de asignación de memoria. Seleccione uno de los **nodos \_ individuales** o  **todos, \_** o uno de los nodos libres o no **libres, \_** o uno de cada par. Cuando especifique más de una opción, separe las opciones con comas.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica otros atributos opcionales de tipo ACF. Cuando especifique más de un atributo de tipo, separe las opciones con comas.

</dd> <dt>

*type-name* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo allocate \]** tiene las siguientes opciones válidas.



| Opción           | Descripción                                                           |
|------------------|-----------------------------------------------------------------------|
| **todos los \_ nodos**   | Realiza una llamada para asignar y liberar memoria para todos los nodos.             |
| **nodo \_ único** | Realiza muchas llamadas individuales para asignar y liberar cada nodo de memoria. |
| **free**         | Libera memoria al devolver el código auxiliar del servidor.                          |
| **no es \_ gratis**   | No libera memoria al devolver desde el código auxiliar del servidor.                  |



 

De forma predeterminada, los códigos auxiliares pueden asignar almacenamiento para los datos a los que hace referencia un puntero único o completo llamando a [**midl \_ user \_ allocate**](midl-user-allocate-1.md) y [**midl \_ user \_ free**](midl-user-free-1.md) individualmente para cada puntero.

Puede optimizar la velocidad de la aplicación especificando la opción **todos los \_ nodos**. Esta opción indica al código auxiliar que calcule el tamaño de toda la memoria a la que se hace referencia a través del puntero del tipo especificado y que realice una única llamada a la asignación de usuario [**medio. \_ \_**](midl-user-allocate-1.md) El código auxiliar libera la memoria realizando una llamada a [**midl \_ user \_ free**](midl-user-free-1.md).

La **opción \_ no** liberar indica al compilador midL que genere un código auxiliar de servidor que no llame a [**midl \_ user \_ free**](midl-user-free-1.md) para el tipo especificado. La **opción \_ no** liberar permite que las estructuras de puntero permanezcan accesibles para la aplicación de servidor después de que la llamada al procedimiento remoto se haya completado y devuelto al cliente.

El **\[ atributo allocate \]** hará que cualquier parámetro **\[ de \]** entrada y salida que sea un puntero a un tipo calificado con la opción todos los nodos para volver a asignar memoria cuando se desmarcan los datos. **\_** Es responsabilidad de la aplicación liberar la memoria asignada anteriormente para este parámetro. Por ejemplo:

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

El código auxiliar reasignará el tipo de [**\[ \]**](out-idl.md) datos PTHISTYPE en la dirección de salida antes de desmarque. Por lo tanto, la aplicación debe liberar la memoria que asignó previamente para los datos de este parámetro o se producirá una pérdida de memoria.

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

[**En**](in.md)
</dt> <dt>

[**asignación de usuario midl \_ \_**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




