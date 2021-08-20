---
description: El método CompareTo \_ del objeto SWbemObject compara dos objetos SWbemObject. Esta comparación está sujeta a ciertas restricciones en función de los valores especificados en el parámetro iFlags.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: SWbemObject.CompareTo_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 70679592c4173596a81f560674879cfa79e0efdd31a735ad8fad72b581cdab31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922443"
---
# <a name="swbemobjectcompareto_-method"></a>Método SWbemObject.CompareTo \_

El **método \_ CompareTo** del [**objeto SWbemObject**](swbemobject.md) compara dos **objetos SWbemObject.** Esta comparación está sujeta a ciertas restricciones en función de los valores especificados en el *parámetro iFlags.*

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objwbemObject* \[ En\]
</dt> <dd>

Obligatorio. Este parámetro es [**un objeto SWbemObject.**](swbemobject.md) Este es el objeto con el que se compara el primer objeto. El objeto debe ser una instancia **de SWbemObject** válida.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Especifica las características del objeto que se deben tener en cuenta al comparar un objeto con otros objetos. Puede usar **wbemComparisonFlagIncludeAll** para tener en cuenta todas las características (este es el valor predeterminado) o cualquier combinación de los valores siguientes.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll** (0 (0x0))


</dt> <dd>

Compara todas las propiedades, calificadores y flavors.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource** (2 (0x2))


</dt> <dd>

Hace que el origen de los objetos, es decir, el servidor y el espacio de nombres del que provenían, se ignore en comparación con otros objetos.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers** (1 (0x1))


</dt> <dd>

Hace que todos los calificadores **(incluidos Key** y **Dynamic)** se ignoren en comparación.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues** (4 (0x4))


</dt> <dd>

Hace que se ignoren los valores predeterminados de las propiedades. Esta marca solo es significativa al comparar clases.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor** (32 (0x20))


</dt> <dd>

Hace que los calificadores se ignoren. Esta marca tiene en cuenta los valores de calificador, pero omite las distinciones de tipo, como las reglas de propagación y las restricciones de invalidación.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase** (16 (0x10))


</dt> <dd>

Compara los valores de cadena de manera que no se diferencian entre mayúsculas y minúsculas. Esto se aplica tanto a las cadenas como a los valores de calificador. Los nombres de propiedades y calificadores siempre se comparan sin distinguir entre mayúsculas y minúsculas, se especifique o no este marcador.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass** (8 (0x8))


</dt> <dd>

Indica al sistema que suponga que los objetos que se comparan son instancias de la misma clase. Por lo tanto, esta marca compara solo la información relacionada con la instancia. Utilice este marcador para optimizar el desarrollo. Si los objetos no son de la misma clase, los resultados no se definen.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve el valor booleano **true si** los objetos coinciden. Devuelve **FALSE si** los objetos no coinciden.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **CompareTo, \_** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




