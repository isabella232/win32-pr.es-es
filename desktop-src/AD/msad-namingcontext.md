---
title: MSAD_NamingContext clase
description: Representa un contexto de nomenclatura (NC) determinado en el controlador de dominio.
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- MSAD_NamingContext clase Active Directory
- MSAD_NamingContext clase Active Directory , descrita
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571f13642116be0e846fe1350cd932d52087d9f0422b8f40d695e4fef99df5cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025783"
---
# <a name="msad_namingcontext-class"></a>Clase MSAD \_ NamingContext

Representa un contexto de nomenclatura (NC) determinado en el controlador de dominio.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a>Miembros

La **clase \_ NamingContext de MSAD** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ NamingContext de MSAD** tiene estas propiedades.

<dl> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene la ruta de acceso X.500 del NC.

</dd> <dt>

**IsFullReplica**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el NC es de lectura y escritura. **TRUE** si el NC es de lectura y escritura; **FALSE** si la NC es de solo lectura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

