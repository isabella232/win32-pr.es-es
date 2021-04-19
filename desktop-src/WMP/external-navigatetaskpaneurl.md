---
title: External. NavigateTaskPaneURL (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. NavigateTaskPaneURL (método)
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Método NavigateTaskPaneURL de Windows Media Player
- Método NavigateTaskPaneURL de Windows Media Player, clase externa
- Clase externa Windows Media Player, método NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698593"
---
# <a name="externalnavigatetaskpaneurl-method"></a>External. NavigateTaskPaneURL (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **NavigateTaskPaneURL** abre una página web en el panel de tareas especificado y cambia el foco al panel especificado.

## <a name="syntax"></a>Sintaxis


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKeyName* \[ de\]
</dt> <dd>

**Cadena** que contiene el nombre de clave de la tienda en línea. (necesario)

</dd> <dt>

*bstrTaskPane* \[ de\]
</dt> <dd>

**Cadena** que contiene el nombre del panel de tareas en el que se abre la Página Web. (necesario)

</dd> <dt>

*bstrParams* \[ de\]
</dt> <dd>

**Cadena** que contiene los parámetros de cadena de consulta que se van a anexar a la dirección URL especificada por el elemento **Navigate** del documento ServiceInfo. (opcional).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Desplazarse a un panel que la tienda en línea no admite puede hacer que la tienda en línea actual cambie.

El valor especificado para *bstrParams* solo es válido cuando se llama a **NavigateTaskPaneURL** desde páginas web proporcionadas por la tienda en línea.

En la tabla siguiente se muestran los valores válidos para *bstrTaskPane* y el panel de tareas asociado para cada uno de ellos.



| Value            | Panel de tareas                      |
|------------------|--------------------------------|
| **ServiceTask1** | Primer panel de tareas de la tienda en línea.  |
| **ServiceTask2** | Segundo panel de tareas de la tienda en línea. |
| **ServiceTask3** | Tercer panel de tareas de la tienda en línea.  |



 

El código de la página web debe especificar un valor para [external. SelectedTaskPane](external-selectedtaskpane.md) al cargar para asegurarse de que se resalta el botón correcto del panel de tareas después de completar la navegación.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo **NavigateTaskPaneURL** crea la dirección URL de la página web que se va a mostrar para **ServiceTask1**.

Ejemplo del elemento **Navigate** :


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



Llamada de ejemplo al método **NavigateTaskPaneURL** :


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



Ejemplo de dirección URL resultante usada para la página web que se muestra en **ServiceTask1**:


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior<br/>                                        |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External. SelectedTaskPane**](external-selectedtaskpane.md)
</dt> </dl>

 

 





