---
description: El método CompareTo \_ del objeto SWbemLastError compara dos objetos SWbemObject. Esta comparación está sujeta a ciertas restricciones en función de los valores especificados en el parámetro iFlags.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: SWbemLastError.CompareTo_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466111"
---
# <a name="swbemlasterrorcompareto_-method"></a>Método SWbemLastError.CompareTo \_

El **método \_ CompareTo** del [**objeto SWbemLastError**](swbemlasterror.md) compara dos [**objetos SWbemObject.**](swbemobject.md) Esta comparación está sujeta a ciertas restricciones en función de los valores especificados en el *parámetro iFlags.*

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

Necesario. Objeto [**de clase SWbemObject.**](swbemobject.md) Este parámetro es el objeto con el que se compara el primer objeto. El objeto debe ser una instancia **de SWbemObject** válida.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Entero que especifica marcas adicionales para la operación. Este parámetro especifica las características del objeto que se deben tener en cuenta cuando se realizan comparaciones de objetos. Puede usar **wbemComparisonFlagIncludeAll** para tener en cuenta todas las características (valor predeterminado) o cualquier combinación de los valores siguientes.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll** (0 (0x0))


</dt> <dd>

Hace que se comparen todas las propiedades, calificadores y flavors.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers** (1 (0x1))


</dt> <dd>

Hace que todos los calificadores **(incluidos Key** y **Dynamic)** se ignoren en la comparación.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource** (2 (0x2))


</dt> <dd>

Hace que el origen de los objetos, es decir, el servidor y el espacio de nombres del que provenían, se ignore en comparación con otros objetos.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues** (4 (0x4))


</dt> <dd>

Hace que se ignoren los valores predeterminados de las propiedades. Esta marca solo es significativa al comparar clases.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass** (8 (0x8))


</dt> <dd>

Indica al sistema que suponga que los objetos que se comparan son instancias de la misma clase. Por lo tanto, esta marca compara solo la información relacionada con la instancia. Utilice este marcador para optimizar el desarrollo. Si los objetos no son de la misma clase, los resultados no se definen.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase** (16 (0x10))


</dt> <dd>

Hace que los valores de cadena se comparen sin tener en cuenta las mayúsculas y minúsculas. Esto se aplica tanto a las cadenas como a los valores de calificador. Los nombres de propiedades y calificadores siempre se comparan sin distinguir entre mayúsculas y minúsculas, se especifique o no este marcador.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor** (32 (0x20))


</dt> <dd>

Hace que se ignoren los formatos de calificador. Este marcador sigue tomando valores del calificador en una cuenta, pero omite las distinciones de modos tales como las reglas de propagación y las restricciones de reemplazamiento.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El **método \_ CompareTo** devuelve el valor **booleano TRUE** si los objetos coinciden; de lo contrario, devuelve **FALSE.**

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método \_ CompareTo,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

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



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemLastError**](swbemlasterror.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




