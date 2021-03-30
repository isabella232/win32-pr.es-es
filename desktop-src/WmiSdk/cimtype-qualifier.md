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
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156829"
---
# <a name="cimtype-qualifier"></a>Calificador CIMType

El calificador **CIMType** contiene texto que describe el tipo de una propiedad.

Este texto puede ser el tipo MOF, como "String" y "sint32", o el tipo CIM, como "CIM \_ String" y "CIM \_ sint32". Hay una correspondencia uno a uno entre el calificador **CIMType** y el tipo de la propiedad que se usa en el parámetro *PvtType* del método [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .

Las dos excepciones son:

-   [*Propiedades de referencia*](gloss-r.md), que tienen el tipo de **\_ referencia CIM**, que contiene el valor "Ref: className". El valor className describe el tipo de clase de la propiedad Reference.
-   Propiedades de objeto incrustado, que tienen el tipo de **\_ objeto CIM** .

Sin embargo, tenga en cuenta que el calificador **CIMType** puede y debe usarse para escribir una propiedad de referencia más exactamente. Por ejemplo, si la propiedad siempre hace referencia a las instancias de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , su calificador **CIMType** debe establecerse en:


```mof
"ref:Win32_LogicalDisk"
```



De forma predeterminada, el calificador **CIMType** de una propiedad de referencia tiene el tipo **ref**.

Al igual que con las propiedades de referencia, el calificador **CIMType** debe usarse para escribir una propiedad de objeto incrustado más exactamente con la sintaxis siguiente:


```mof
"object:EmbedClass"
```



Dado que WMI permite más tipos de los que se pueden expresar mediante constantes estándar con el \_ prefijo VT, el calificador **CIMType** puede ayudar a interpretar los valores de tipo. El calificador **CIMType** se agrega automáticamente. Para obtener más información, vea [tipos de datos MOF](mof-data-types.md).

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

[Adición de un calificador](adding-a-qualifier.md)
</dt> </dl>

 

