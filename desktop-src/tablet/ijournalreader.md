---
description: Proporciona acceso de lectura a un archivo de Windows Journal y devuelve una secuencia que contiene una versión XML del contenido del archivo.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Interfaz IJournalReader (Journal. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361581"
---
# <a name="ijournalreader-interface"></a>Interfaz IJournalReader

Proporciona acceso de lectura a un archivo de Windows Journal y devuelve una secuencia que contiene una versión XML del contenido del archivo.

> [!Note]  
> El componente lector del diario no puede leer archivos de Windows Journal creados por equipos que ejecutan Windows 7 o posterior. La interfaz IJournalReader se debe considerar en desuso u obsoleta y no debe usarse.

 

## <a name="members"></a>Miembros

La interfaz **IJournalReader** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IJournalReader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IJournalReader** tiene estos métodos.



| Método                                                  | Descripción                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**ReadFromStream**](ijournalreader-readfromstream.md) | Toma un flujo a un archivo de notas de Journal y devuelve una secuencia XML que representa el contenido del documento.<br/> |



 

## <a name="remarks"></a>Observaciones

La clase **JournalReader** permite cargar un flujo de documento de diario y recibir una secuencia XML que representa el contenido. Puede reconstituir, mostrar y manipular la tinta.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente de un controlador del evento [**click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de un botón se crea una instancia de la clase **JournalReader** y se usa para leer un archivo de diario existente.

> [!Note]  
> No se muestra el método **DisplayXml** al que se llama desde este ejemplo. La implementación específica de este tipo de método depende de las necesidades de la aplicación.

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                         |
| Encabezado<br/>                   | <dl> <dt>Journal. h (también requiere Journal \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GUID de propiedad personalizada](custom-property-guids.md)
</dt> <dt>

[**Método ReadFromStream**](ijournalreader-readfromstream.md)
</dt> </dl>

 

