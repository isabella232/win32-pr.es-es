---
description: El calificador CIMType contiene texto que describe el tipo de una propiedad.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Calificador CIMType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 86fad829bf1b2391a9bc97d5c6281a67cadae7d03672e8a6eb8093b7ff6152b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131677"
---
# <a name="cimtype-qualifier"></a>Calificador CIMType

El **calificador CIMType** contiene texto que describe el tipo de una propiedad.

Este texto puede ser el tipo MOF como "string" y "sint32" o el tipo CIM, como "CIM STRING" y \_ "CIM \_ SINT32". Hay una correspondencia uno a uno entre el calificador **CIMType** y el tipo de la propiedad usada en el parámetro *pvtType* del [**método IWbemClassObject::Get.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)

Las dos excepciones son:

-   [*Propiedades de*](gloss-r.md)referencia , que tienen el tipo **CIM \_ REFERENCE**, que contiene el valor "REF:classname". El valor classname describe el tipo de clase de la propiedad de referencia.
-   Propiedades de objeto incrustadas, que tienen el **tipo \_ CIM OBJECT.**

Tenga en cuenta, sin embargo, que el **calificador CIMType** puede y debe usarse para escribir una propiedad de referencia con más exactitud. Por ejemplo, si la propiedad siempre hace referencia a instancias de la clase [**\_ LogicalDisk de Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) su **calificador CIMType** debe establecerse en:


```mof
"ref:Win32_LogicalDisk"
```



De forma predeterminada, el **calificador CIMType** de una propiedad de referencia tiene el tipo **ref**.

Al igual que con las propiedades de referencia, el **calificador CIMType** debe usarse para escribir una propiedad de objeto incrustado más exactamente con la sintaxis siguiente:


```mof
"object:EmbedClass"
```



Dado que WMI permite expresar más tipos de los que se pueden expresar mediante constantes estándar con el prefijo VT, el calificador \_ **CIMType** puede ayudar a interpretar los valores de tipo. El **calificador CIMType** se agrega automáticamente. Para obtener más información, vea [Tipos de datos MOF](mof-data-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores WMI estándar**](standard-wmi-qualifiers.md)
</dt> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Agregar un calificador](adding-a-qualifier.md)
</dt> </dl>

 

