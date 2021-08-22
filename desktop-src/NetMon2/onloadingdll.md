---
description: Carga el archivo DLL del monitor.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Función OnLoadingDLL (Netmon.h)
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
ms.openlocfilehash: 6049684798d6dda9030abd667c28a62f4b19f9b4e66a831ef4c1d2caa880fb1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676875"
---
# <a name="onloadingdll-function"></a>Función OnLoadingDLL

La **función OnLoadingDLL** carga el archivo DLL del monitor.

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

Blob que usa MCSVC para hacer coincidir un monitor con NIC disponibles. Este parámetro siempre contiene una solicitud para una [interfaz IRTC,](irtc.md) por lo que la mayoría de los monitores no necesitan agregar ninguna entrada al BLOB. Sin embargo, un monitor personalizado puede agregar criterios de filtro adicionales (por ejemplo, que el tipo MAC debe ser Ethernet).

</dd> <dt>

*pCreateFlags* \[ En\]
</dt> <dd>

Marcas que indican cómo MCSVC controla la creación de un monitor. Este parámetro debe ser uno de los siguientes valores:



| Value                                                                                                                                                                                                            | Significado                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ CREATE \_ ONE \_ PER \_ NETCARD**</dt> </dl>          | MCSVC garantiza que solo existe una instancia de este monitor para cada NIC. Solo se puede crear una segunda instancia si se destruye la primera.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**MCS \_ CREA \_ CONFIGURACIONES DE FORMA \_ \_ PREDETERMINADA**</dt> </dl> | Si el monitor tiene una configuración interna predeterminada, MCSVC no requiere que el usuario configure el monitor antes de crear la instancia.<br/>  |



 

</dd> <dt>

*ppDefaultName* \[ out\]
</dt> <dd>

Puntero a un puntero a la dirección del nombre predeterminado del monitor. MCSVC usa el nombre predeterminado al crear instancias del monitor.

Por ejemplo, si el nombre predeterminado devuelto es "Monitor de enrutador", la primera instancia de monitor sería "Monitor de enrutador 1", la segunda sería "RouterMonitor2, y así sucesivamente. Si se devuelve **NULL,** MCSVC usa el nombre del archivo DLL.

</dd> <dt>

*ppDescription* \[ out\]
</dt> <dd>

Puntero a un puntero a la dirección de la descripción del monitor. La descripción se pasa a la Herramienta de control de supervisión, que usa la descripción para indicar al usuario que el monitor existe. Este parámetro puede devolver **NULL.**

</dd> <dt>

*ppDefaultScript* \[ out\]
</dt> <dd>

Puntero a un puntero a la dirección del script de formulario HTML predeterminado que se usa para configurar el monitor. Aunque las instancias del monitor pueden modificar su propio script, la mayoría de los monitores simplemente cargan su script una vez, desde un archivo. El valor de *ppDefaultScript* puede ser **NULL**; sin embargo, el monitor no se puede configurar externamente o debe proporcionar un script más adelante. Es más eficaz proporcionar un script predeterminado aquí.

</dd> <dt>

*ppDefaultConfig* \[ out\]
</dt> <dd>

Dirección de la cadena predeterminada que se usa para configurar el monitor cuando se crea. Este parámetro se puede establecer en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es S \_ OK, que es el mismo que NOERROR.

Si la función no se realiza correctamente, MCSVC omite el monitor especificado de todas sus listas; después, no se puede crear ningún monitor de este tipo.

## <a name="remarks"></a>Comentarios

McSVC llama una vez a la función **OnLoadingDLL** cuando carga por primera vez el archivo DLL. A continuación, el archivo DLL proporciona los valores predeterminados que usará MCSVC al crear una instancia de un monitor.

El monitor debe asignar toda la memoria necesaria para las cadenas devueltas a MCSVC. En la devolución, MCSVC realiza copias de todas las cadenas y no intentará liberar las cadenas devueltas.

El monitor debe usar las funciones auxiliares de BLOB para modificar el blob de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




