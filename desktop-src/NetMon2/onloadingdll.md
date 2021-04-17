---
description: Carga el archivo DLL del monitor.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Función OnLoadingDLL (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677455"
---
# <a name="onloadingdll-function"></a>OnLoadingDLL función)

La función **OnLoadingDLL** carga el archivo dll de supervisión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFilterBlob* \[ in, out\]
</dt> <dd>

Un BLOB que utiliza el MCSVC para que coincida con un monitor con NIC disponibles. Este parámetro siempre contiene una solicitud de una interfaz [IRTC](irtc.md) , por lo que la mayoría de los monitores no necesitan agregar entradas al BLOB. Sin embargo, un monitor personalizado puede Agregar criterios de filtro adicionales (por ejemplo, que el tipo MAC debe ser Ethernet).

</dd> <dt>

*pCreateFlags* \[ de\]
</dt> <dd>

Marcas que indican cómo el MCSVC controla la creación de un monitor. Este parámetro debe ser uno de los siguientes valores:



| Value                                                                                                                                                                                                            | Significado                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ crear \_ uno \_ por \_ tarjeta de**</dt> </dl>          | MCSVC garantiza que solo existe una instancia de este monitor para cada NIC. Solo se puede crear una segunda instancia si se destruye la primera.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**\_crear \_ configuraciones de MCS \_ de forma \_ predeterminada**</dt> </dl> | Si el monitor tiene una configuración interna predeterminada, MCSVC no requiere que el usuario configure el monitor antes de crear la instancia.<br/>  |



 

</dd> <dt>

*ppDefaultName* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a la dirección del nombre predeterminado del monitor. MCSVC usa el nombre predeterminado al crear instancias del monitor.

Por ejemplo, si el nombre predeterminado devuelto es "router monitor", la primera instancia del monitor sería "router monitor 1", la segunda sería "RouterMonitor2, etc. Si se devuelve **null** , MCSVC utiliza el nombre del archivo dll.

</dd> <dt>

*ppDescription* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a la dirección de la descripción del monitor. La descripción se pasa a la herramienta supervisar control, que usa la descripción para indicar al usuario que el monitor existe. Este parámetro puede devolver **null**.

</dd> <dt>

*ppDefaultScript* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a la dirección del script de formulario HTML predeterminado que se usa para configurar el monitor. Aunque las instancias del monitor pueden modificar su propio script, la mayoría de los monitores simplemente cargan su script una vez, desde un archivo. El valor de *ppDefaultScript* puede ser **null**; sin embargo, el monitor no se puede configurar externamente o debe proporcionar un script más adelante. Es más eficaz proporcionar aquí un script predeterminado.

</dd> <dt>

*ppDefaultConfig* \[ enuncia\]
</dt> <dd>

La dirección de la cadena predeterminada que se usa para configurar el monitor cuando se crea. Este parámetro se puede establecer en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es S \_ OK; que es igual que NoError.

Si la función no se realiza correctamente, MCSVC omite el monitor especificado de todas sus listas; después de, no se puede crear ningún monitor de este tipo.

## <a name="remarks"></a>Observaciones

El MCSVC llama a la función **OnLoadingDLL** una vez, la primera vez que carga el archivo dll. A continuación, el archivo DLL proporciona los valores predeterminados que usará el MCSVC al crear una instancia de un monitor.

El monitor debe asignar toda la memoria necesaria para las cadenas que se devuelven a MCSVC. En la devolución, el MCSVC realiza copias de todas las cadenas y no intenta liberar las cadenas devueltas.

El monitor debe usar las funciones auxiliares de BLOB para modificar el BLOB de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




