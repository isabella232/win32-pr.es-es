---
description: Cree un nuevo elemento secundario. Agrega objetos IWiaItem2 al árbol IWiaItem2 de un dispositivo.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: Método IWiaItem2::CreateChildItem (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e7d7215f528c36f6b4f5883be19d5d37c8b76d4d8ad9cacbcaa7a63397337c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965574"
---
# <a name="iwiaitem2createchilditem-method"></a>IWiaItem2::CreateChildItem (método)

Cree un nuevo elemento secundario. Agrega [**objetos IWiaItem2**](-wia-iwiaitem2.md) al árbol **IWiaItem2** de un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lItemFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica el tipo de elemento WIA 2.0. Vea [**Marcas de tipo de elemento de WIA.**](-wia-wia-item-type-flags.md)

</dd> <dt>

*lCreationFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica cómo crear el nuevo elemento.

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0)


</dt> <dd>

Establezca los valores predeterminados para las propiedades del elemento secundario.

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY \_ VALORES \_ DE \_ PROPIEDAD PRIMARIOS** (0x40000000)


</dt> <dd>

Copie los valores de todas las propiedades de lectura y escritura del elemento primario.

</dd> </dl> </dd> <dt>

*bstrItemName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del elemento. Este nombre se anexa al final del nombre del elemento primario para generar el nombre completo del elemento.

</dd> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero a la [**interfaz IWiaItem2**](-wia-iwiaitem2.md) que establece el **método IWiaItem2::CreateChildItem.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Algunos dispositivos de hardware WIA 2.0 permiten a las aplicaciones crear nuevos elementos en el árbol [**IWiaItem2**](-wia-iwiaitem2.md) que representa el dispositivo. Las aplicaciones deben probar los dispositivos para ver si admiten esta funcionalidad. Use la interfaz CAPS de IEnumWIA \_ DEV \_ para enumerar las funcionalidades del dispositivo actual.

Si el dispositivo permite la creación de nuevos elementos en el árbol [**IWiaItem2,**](-wia-iwiaitem2.md) la invocación de **IWiaItem2::CreateChildItem** crea un nuevo objeto **IWiaItem2** que es un elemento secundario del nodo actual. Pasa un puntero al nuevo nodo a la aplicación a través del *parámetro ppIWiaItem2.* Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del *parámetro ppIWiaItem2.*

Si *lCreationFlags es* COPY \_ PARENT PROPERTY VALUES y \_ \_ *lItemFlags* es cero, la función devuelve E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
