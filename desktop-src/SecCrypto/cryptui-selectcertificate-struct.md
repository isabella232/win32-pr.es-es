---
description: Contiene información sobre el cuadro de diálogo que muestra la función CryptUIDlgSelectCertificate.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: Estructura de CRYPTUI_SELECTCERTIFICATE_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669738"
---
# <a name="cryptui_selectcertificate_struct-structure"></a>\_SELECTCERTIFICATE \_ estructura de estructura CRYPTUI

La estructura de estructura **CRYPTUI \_ \_ SELECTCERTIFICATE** contiene información sobre el cuadro de diálogo que muestra la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tamaño, en bytes, de esta estructura.

</dd> <dt>

**hwndParent**
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo. Si este valor es **null**, la ventana primaria es la ventana de escritorio predeterminada.

</dd> <dt>

**dwFlags**
</dt> <dd>

Especifica opciones adicionales para la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) . Puede ser cero o **una operación OR bit a bit** de los valores siguientes.



| Value                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt> </dl>                              | Reservado.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ heredado**</dt> </dl>                                       | Especifica que se va a mostrar el cuadro de diálogo heredado.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ MultiSelect**</dt> </dl>                        | Permite al usuario seleccionar más de un certificado en el cuadro de diálogo. Si se establece esta marca, la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) siempre devuelve **null**. El miembro **hSelectedCertStore** de esta estructura debe contener un identificador para un almacén de certificados. Los certificados seleccionados por el usuario se agregarán a este almacén.<br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <dt>**\_ \_ \_ \_ nivel superior de la ventana de SELECTCERT de CRYPTUI**</dt> </dl> | Obliga a que la interfaz de usuario de criptografía sea la ventana superior de la pantalla.<br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**szTitle**
</dt> <dd>

Título para mostrar del cuadro de diálogo. Si el valor de este miembro es **null**, se usa el título predeterminado de "seleccionar certificado".

</dd> <dt>

**dwDontUseColumn**
</dt> <dd>

Marcas que se pueden combinar para excluir columnas de la pantalla.



| Value                                                                                                                                                                                                                                                                                       | Significado                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ ISSUED to \_ Column**</dt> <dt>1 (0x1)</dt> </dl>             | No Mostrar información de **emitido** .<br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <dt>**CRYPTUI \_ SELECCIONAR \_ ISSUEDBY \_ columna**</dt> <dt>2 (0X2)</dt> </dl>             | No Mostrar información de **ISSUEDBY** .<br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <dt>**CRYPTUI \_ SELECCIONAR \_ INTENDEDUSE \_ columna**</dt> <dt>4 (0x4)</dt> </dl>    | No Mostrar información de **IntendedUse** .<br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <dt>**CRYPTUI \_ SELECCIONAR \_ FRIENDLYNAME \_ columna**</dt> <dt>8 (0x8)</dt> </dl> | No Mostrar información del nombre.<br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <dt>**CRYPTUI \_ SELECCIONAR \_ Ubicación \_ columna**</dt> <dt>16 (0x10)</dt> </dl>           | No Mostrar información de ubicación.<br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <dt>**CRYPTUI \_ Seleccionar \_ la \_ columna de expiración**</dt> <dt>32 (0x20)</dt> </dl>     | No Mostrar información de expiración.<br/>      |



 

</dd> <dt>

**szDisplayString**
</dt> <dd>

Texto que se muestra en el cuadro de diálogo para indicar al usuario. Si el valor de este miembro es **null**, se usa la cadena predeterminada "Seleccione un certificado que desee usar".

</dd> <dt>

**pFilterCallback**
</dt> <dd>

Puntero a una función de devolución de llamada [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) que filtra los certificados que se muestran en el cuadro de diálogo.

</dd> <dt>

**pDisplayCallback**
</dt> <dd>

Puntero a una función de devolución de llamada [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) que muestra los certificados que el usuario selecciona para su visualización.

</dd> <dt>

**pvCallbackData**
</dt> <dd>

Datos adicionales que se pasan a las funciones de devolución de llamada especificadas por los miembros **pFilterCallback** y **pDisplayCallback** .

</dd> <dt>

**cDisplayStores**
</dt> <dd>

El número de almacenes de certificados en la matriz **rghDisplayStores** .

</dd> <dt>

**rghDisplayStores**
</dt> <dd>

Puntero a una matriz de almacenes que contienen certificados disponibles para la selección en el cuadro de diálogo.

</dd> <dt>

**cStores**
</dt> <dd>

El número de almacenes de certificados en la matriz **rghStores** .

</dd> <dt>

**rghStores**
</dt> <dd>

Puntero a una matriz de almacenes de certificados en los que se va a buscar al compilar una cadena de certificados y comprobar la confianza de los certificados mostrados en el cuadro de diálogo.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

El número de páginas de propiedades de la matriz **rgPropSheetPages** .

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Puntero a una matriz de estructuras **PROPSHEETPAGE** que representan las páginas de propiedades que se pasan al cuadro de diálogo visualización de certificados cuando se selecciona un certificado para su visualización.

</dd> <dt>

**hSelectedCertStore**
</dt> <dd>

Identificador de un almacén de certificados creado por el autor de la llamada. Los certificados seleccionados por el usuario se agregan a este almacén. Si el número de certificados de este almacén es el mismo antes y después de llamar a [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), el usuario ha cerrado el cuadro de diálogo sin seleccionar ningún certificado.

Este miembro no se usa si el miembro **dwFlags** de esta estructura no contiene el marcador **de \_ \_ selección MultiSelect CRYPTUI SELECTCERT** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                            |
| Nombres Unicode y ANSI<br/>   | **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) y **CRYPTUI \_ SELECTCERTIFICATE \_ Structa** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




